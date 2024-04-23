# MCTS_Heuristic
MCTS Heuristic to play Connect 4  

Code update from:  
alphazero_connect4/MCTS_vs_Alphazero/connect4_selfplay_mcts_vs_Alphazero_colab.ipynb    

Only update inside Node_Orig Class, simulate function:    
1. always select winning moves if available (highest priority)   
2. always block opponent's winning moves if we have no winning move (medium priority)  
3. otherwise random rollout on valid move (lowest priority)  

Heuristic idea comes from below:  
https://github.com/Carbon225/mctx-classic   
