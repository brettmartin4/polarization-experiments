# polarization-experiments
Data for the polarization paper

Test start time in posix:
1696225320000

End time is: 
1696262370000

### TODO:

For each model:

Baseline:
 - model_str at top
 - model_name and tuned_ver after
 - create baseline model with init params
 - fit model
 - generate predictions on tr and va sets (yhat)
 - print metrics, save preds, and plot results

Tuned:
 - model_name and tuned_ver at top
 - set rng
 - set N_trials
 - search for best_params and best model in for loop
 - CHANGE TO EVAL ON RMSE INSTEAD OF R2
 - generate predictions on tr and va sets (yhat)
 - print metrics, log hyperparams, save preds, and plot results

TSCV:
 - set best_params
 - print tscv metrics after for loop



SVR:
 - remove 2nd block
 - remove 3rd block
 - include model_name and tuned_ver in block 4
 - remove last several lines from block 4 starting with rmse_tr assignment
 - add statements to print metrics, log hyperparams, save preds, and plot results
 - remove last several lines
 - print tscv metrics

RF:
 - model_str at top
 - model_name and tuned_ver after
 - remove print shapes statement
 - Remove everything starting from the RandomForest Baseline print statement
 - add statements to print metrics, log hyperparams, save preds, and plot results
 - Move everything from est_grid assignment to new block
 - In new block, model_name and tuned_ver at top
 - Remove everything after model predictions (yhat assignments)
 - add statements to print metrics, log hyperparams, save preds, and plot results
 - in tscv: get rid of H maybe?
 - remove everything after loop.
 - print tscv metrics after for loop

MLP:
 - see if I can move np and tf seeding to reset_tf_state function call
 - Change standard scaling to min-max scaling between -1 and 1
 - move data separation to separate block
 - Figure out wtf is going on with these model predictions
 - Move tuned model stuff to new block
 - add functions to both blocks for printing, plotting, and saving
 - for tscv, see if I can remove all y_prev references for skill
 - add function calls in tscv block

 - remove all "verbose" arguments from calls to NN fit

