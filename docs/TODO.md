# Things to do

## Example Projects and Demonstrations for Aerostack2 Swarm Drones

### 1. **Dynamic Formation Control**
- **Objective**: Demonstrate multi-drone formation flying with various geometric patterns (line, V-shape, triangle, grid)
- **Key Features**:
  - Real-time formation switching between different configurations
  - Adaptive formation scaling based on target area
  - Formation integrity maintenance during GPS denied environments
  - Trajectory tracking with coordinated velocity profiles
- **Use Cases**: Area surveillance, perimeter monitoring, cooperative transportation
- **Implementation Approach**: Extend behavior trees with formation switching logic; implement differential flatness controller for smooth transitions

### 2. **Collaborative Swarm Exploration & Mapping**
- **Objective**: Autonomous exploration of unknown environments with distributed frontier-based exploration
- **Key Features**:
  - Decentralized frontier detection and assignment
  - Real-time consensus-based exploration planner
  - Simultaneous mapping using onboard cameras
  - Dynamic replanning based on discovered obstacles
- **Use Cases**: Search and rescue, environmental monitoring, infrastructure inspection
- **Implementation Approach**: Integrate mission interpreter with exploration algorithms; use behavior trees for exploration state machine

### 3. **Cooperative Target Tracking & Encirclement**
- **Objective**: Swarm of drones autonomously track and encircle a moving target while maintaining formation
- **Key Features**:
  - Distributed target detection and tracking
  - Dynamic encirclement with configurable radius
  - Adaptive spacing based on target velocity
  - Camera-based and GPS-based tracking modes
- **Use Cases**: Wildlife monitoring, moving object surveillance, target interception
- **Implementation Approach**: Leverage camera calibration; implement consensus-based target estimation; use PID speed controller for smooth tracking

### 4. **Multi-Agent Path Planning with Collision Avoidance**
- **Objective**: Demonstrate decentralized collision avoidance with optimal path planning for multiple drones
- **Key Features**:
  - Reciprocal collision avoidance between agents
  - Optimal trajectory planning avoiding static/dynamic obstacles
  - Velocity obstacle computation for swarm members
  - Deadlock resolution in congested scenarios
- **Use Cases**: Warehouse navigation, traffic management in urban airspace, complex choreography
- **Implementation Approach**: Integrate graph-based planners with distributed velocity obstacle algorithms; extend behavior trees with avoidance logic

### 5. **Heterogeneous Swarm Coordination**
- **Objective**: Coordinate mixed drone types with different capabilities (sensors, payloads, speed profiles)
- **Key Features**:
  - Task allocation based on drone capabilities
  - Adaptive speed and altitude coordination for mixed swarms
  - Leader-follower coordination with heterogeneous dynamics
  - Capability-aware mission decomposition
- **Use Cases**: Hybrid surveillance (fast scouts + slow sensors), collaborative manipulation, emergency response
- **Implementation Approach**: Extend mission interpreter to support capability constraints; implement capability-aware task assignment in behavior trees

### 6. **Distributed Cooperative Manipulation & Payload Transfer**
- **Objective**: Swarm drones work together to manipulate or transport shared payloads between locations
- **Key Features**:
  - Coordinated lift-off and landing procedures
  - Force/torque distribution for stable payload control
  - Real-time payload state estimation
  - Graceful handoff between drone teams
- **Use Cases**: Construction, logistics in GPS-denied areas, emergency supply delivery
- **Implementation Approach**: Design specialized behavior trees for manipulation; implement force feedback from airframes; develop payload dynamics model

### 7. **Network-Aware Swarm Mission Execution**
- **Objective**: Execute complex collaborative missions while accounting for communication constraints and network topology
- **Key Features**:
  - Communication graph-aware mission planning
  - Deployment of relay drones to maintain connectivity
  - Graceful degradation under communication loss
  - Multi-hop message routing within swarm
  - Mission rollback and recovery procedures
- **Use Cases**: Beyond line-of-sight operations, autonomous swarm in challenging environments, resilient multi-team coordination
- **Implementation Approach**: Extend tmuxinator configs for distributed network simulation; implement mission state synchronization protocols; add communication-aware constraints to path planners