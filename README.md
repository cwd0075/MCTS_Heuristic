# MCTS_Heuristic
MCTS Heuristic to play Connect 4  

Code update from:  
alphazero_connect4/MCTS_vs_Alphazero/connect4_selfplay_mcts_vs_Alphazero_colab.ipynb    

Only update inside Node_Orig Class, simulate function:    
1. always select winning moves if available (highest priority)   
2. always block opponent's winning moves if we have no winning move (medium priority)  
3. otherwise random rollout on valid move (lowest priority)  

### Heuristic idea comes from below:  
it use Heuristic Policy Function during rollout (simulate) phase in MCTS  
https://github.com/Carbon225/mctx-classic   

### Other MCTS Heuristic implementation:  
Greedy-mcts, AlphaMCTS with a Heuristic Value Function  
https://github.com/lowrollr/turbozero_torch/wiki/Evaluation-&-Testing#greedy-mcts 
https://github.com/lowrollr/turbozero_torch/blob/e9283ad5002fcbea95ebe977c7731aa218eb15c6/envs/othello/env.py#L190  
It use get_greedy_rewards as the value function during evaluation phase (rollout or simulate phase). While the policy function is using uniform_probabilities. So it is AlphaMCTS, not pure MCTS   

### Other info found online:  
https://www.reddit.com/r/ComputerChess/comments/l0ps52/can_you_combine_mcts_with_an_evaluation_function/   
https://m-m-moghadam.medium.com/monte-carlo-tree-search-improving-the-rollouts-using-the-rapid-action-value-estimation-rave-be2a23c1b72b  
https://m-m-moghadam.medium.com/monte-carlo-tree-search-improving-the-rollouts-using-the-decisive-move-last-good-reply-lgr-6d2264fffedb   

