// Function to simulate an asynchronous operation
function simulateAsyncOperation(value, delay) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (value) {
        resolve(Operation successful: ${value});
      } else {
        reject(new Error('Operation failed.'));
      }
    }, delay);
  });
}

// Async function to handle asynchronous operations
async function performAsyncOperations() {
  try {
    console.log('Starting async operations...');
    
    const result1 = await simulateAsyncOperation('First', 2000);
    console.log(result1);
    
    const result2 = await simulateAsyncOperation('Second', 1500);
    console.log(result2);
    
    const result3 = await simulateAsyncOperation('Third', 1000);
    console.log(result3);
    
    console.log('All async operations completed.');
  } catch (error) {
    console.error('Error:', error.message);
  }
}

// Call the async function to initiate the asynchronous operations
performAsyncOperations();
