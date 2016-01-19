% runExample.m ------------------------------------------------------------
%
% This script shows one possible approach to identifying solar panels in
% satellite imagery data using machine learning. This demonstrates the
% basic process of machine learning, but is not an optimized algorithm
% (that's where you come it!). You're encouraged to innovate on each step
% in this process from preprocessing, feature extraction, classification,
% and validation.
%
% Author: Kyle Bradbury
% Organization: Duke University Energy Initiative
% Date: 19 January 2016

%--------------------------------------------------------------------------
% Testbed for exploring machine learning techniques
%--------------------------------------------------------------------------

% -- Load data and initialize parameters -----------------------------
% Initialize parameters
imageDirectory    = './train/' ;       % Adjust this directory to point to your image files
solutionDirectory = './solution/' ;    % Adjust this directory to point to your training label/solution files
kFolds            = 5 ;                % Number of folds for cross validation
submissionFile    = 'submission.csv' ; % Output csv submission filename

% Load the training data solution
labelsRaw = csvread([solutionDirectory 'train_solution.csv'],1,0) ; % Extract the class labels
labels = sortrows(labelsRaw,1) ; % In case their not in ascending order, sort them
labels = labels(:,2) ; % Remove the id since they are now in order and therefore can be indexed by their ids

nObservations = length(labels) ; % Total number of observations

% -- Extract feature vectors -----------------------------------------
for iObservation = 1:nObservations
    % Load each image
    cImage = imread(sprintf('%simage%g.tif',imageDirectory,iObservation),'tif') ;
    
    % Extract features from the image
    features(1,2) = [mean(cImage(:)) std(cImage(:))] ;
end

% -- Conduct cross-validated training of the data --------------------
partition = cvpartition(nObservations,'KFold',kFolds) ; % This creates a cvpartition class object for the cross validation

for iFold = 1:kFolds % For each fold of the partition
    
end




% Display ROC curve


%--------------------------------------------------------------------------
% Train classifier on training data and run on test data to produce results
% for submission to Kaggle
%--------------------------------------------------------------------------

% Train the classifier on all of the training data

% Run the classifier on the test data

% Output the results