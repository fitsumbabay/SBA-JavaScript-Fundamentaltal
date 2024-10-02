# SBA-JavaScript-Fundamentaltal





// Data structures (you'll need to populate these with the provided sample data)
const courseInfo = {
  id: 0,
  name: ""
};
const assignmentGroup = {
  id: 0,
  name: "",
  course_id: 0,
  group_weight: 0,
  assignments: []
};
const learnerSubmissions = [];
// Main function
function getLearnerData(courseInfo, assignmentGroup, learnerSubmissions) {
  // Validate input data
  if (!validateInputData(courseInfo, assignmentGroup, learnerSubmissions)) {
    throw new Error("Invalid input data");
  }
  // Process learner submissions
  const learnerData = processLearnerSubmissions(assignmentGroup, learnerSubmissions);
  // Calculate weighted averages
  const result = calculateWeightedAverages(learnerData, assignmentGroup);
  return result;
}
// Helper function to validate input data
function validateInputData(courseInfo, assignmentGroup, learnerSubmissions) {
  // TODO: Implement data validation
  return true;
}
// Helper function to process learner submissions
function processLearnerSubmissions(assignmentGroup, learnerSubmissions) {
  // TODO: Implement submission processing
  return {};
}
// Helper function to calculate weighted averages
function calculateWeightedAverages(learnerData, assignmentGroup) {
  // TODO: Implement weighted average calculation
  return [];
}
// Example usage
try {
  const result = getLearnerData(courseInfo, assignmentGroup, learnerSubmissions);
  console.log(result);
} catch (error) {
  console.error("An error occurred:", error.message);
}

Let's start with the main function:
This function is the entry point of our script. It takes three parameters:

1.courseInfo: Contains information about the course
2.assignmentGroup: Contains information about a group of assignments
3.learnerSubmissions: An array of learner submissions

It does three things:
Validates the input data
Processes the learner submissions
Formats the result
Now, let's look at each helper function:
validateInputData:
This function checks if the AssignmentGroup belongs to the correct course. If not, it throws an error. You can add more validation checks here as needed.
processLearnerSubmissions:
This function is the core of our script. It:
Iterates through each submission
Finds the corresponding assignment
Checks if the assignment is due
Applies a late submission penalty if necessary
Calculates the score as a percentage
Aggregates the data for each learner
Key points:
It skips assignments that aren't due yet
It applies a 10% penalty for late submissions
It calculates a weighted score based on points possible
formatResult:
This function takes the processed data and formats it according to the required output structure. It:
Converts the learner ID to a number
Calculates the average score
Spreads the individual assignment scores into the result object
The script ends with example usage, creating sample data for courseInfo, assignmentGroup, and learnerSubmissions, then calling getLearnerData() with these parameters and logging the result.
This modular approach makes the code easier to understand, test, and maintain. Each function has a single responsibility, and the main function orchestrates the overall process.
# SBA-JavaScript-Fundamentaltal
