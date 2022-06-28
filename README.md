# theRLSnake
A Reinforcement Learning Agent: Snake, optimizes its actions according to the Deep Q-Learning Algorithm. 


![Alt Text](https://media.geeksforgeeks.org/wp-content/uploads/20210611151042/Animation.gif)



# Reinforcement Learning
Reinforcement learning is an area of machine learning concerned with how intelligent agents ought to take actions in an environment in order to maximize the notion of cumulative reward.
Simply, reinforcement learning is teaching a software agent how to behave in an environment by telling it how good it's doing.
## Agent : Snake
## Environment : the game 
## Reward: scores given to determine which actions the snake should take in order to move to the next state. 

# Part 1:
## Agent:
- game
- model
training:
- state = get_state(game)
- action = get_move(state):
           -model.predict()
- reward, game_over, score = game.play_step(action)
- new_state = get_state(game)
- remember
- model.train()

## Game(Pygame)
- play_step(action)
  -reward, game_over, score
  
## Model(PyTorch)
Linear_QNet(DQN)
- model.predict(state)
  -action
  
## Action
[1, 0, 0] -> striaght\
[0, 1, 0] -> right turn\
[0, 0, 1] -> left turn

## State(11 values)
- danger straight
- danger right
- danger left
- direction up
- direction down
- direction left
- direction right
- food left
- food right
- food up
- food down
example:


@@@@@@@@@@@@@@\
---------------->\
                   []
                   
                   
  actions:\
  [0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 1]
                   
                   
  
