# Manual hunk edit mode -- see bottom for a quick guide.
@@ -94,34 +104,51 @@ public class ProductService : IProductService
             var sellerId = _currentUser.UserId
                            ?? throw new UnauthorizedAccessException("User is not authenticated.");
 

+
             var product = await _repository.GetByIdAsync(id);
+
             if (product == null)
+            {

                 throw new NotFoundException($"Product with ID {id} not found.");
-            
+            }
+
             if (product.SellerId != sellerId)

 
-            _mapper.Map(dto, product);

 
             await _repository.UpdateAsync(product);
             await _unitOfWork.SaveChangesAsync();
 

+
             return _mapper.Map<ProductDto>(product);
         }
 
         public async Task<bool> DeleteProductAsync(int id)
         {
+            //(DeletSection)
             var sellerId = _currentUser.UserId
                            ?? throw new UnauthorizedAccessException("User is not authenticated.");
 
             var product = await _repository.GetByIdAsync(id);
+            
+            //check if product exists
             if (product == null)
-                throw new NotFoundException($"Product with ID {id} not found.");
+                throw new NotFoundException("Product with ID {id} not found.");
             
             //security check: ownership
             if (product.SellerId != sellerId)
+            {
                 _logger.LogWarning("Unauthorized delete attempt by user {SellerId} on product {ProductId}", sellerId, id);
                 throw new UnauthorizedAccessException("You do not have permission to delete this product.");
+
+            }
                 
             //Delete
             await _repository.DeleteAsync(product);
# ---
# To remove '-' lines, make them ' ' lines (context).
# To remove '+' lines, delete them.
# Lines starting with # will be removed.
# If the patch applies cleanly, the edited hunk will immediately be marked for staging.
# If it does not apply cleanly, you will be given an opportunity to
# edit again.  If all lines of the hunk are removed, then the edit is
# aborted and the hunk is left unchanged.
