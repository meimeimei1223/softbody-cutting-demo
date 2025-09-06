# Soft Body Deformation & Cutting Demo

An interactive WebGL-based physics simulation showcasing real-time soft body deformation and cutting mechanics using tetrahedral mesh algorithms.

## 🎯 Features

### Interactive Simulation Modes
- **🎯 Deform Mode**: Click and drag to deform the soft body mesh with realistic physics response
- **✂️ Cut Mode**: Slice through the mesh using precise tetrahedral cutting algorithms
- **⚓ Anchor Mode**: Pin vertices in place to create fixed constraint points (max 3)
- **✨ Smooth Mode**: Apply Laplacian smoothing operations to refine mesh geometry

### Advanced Physics
- Position-based dynamics (PBD) simulation
- Tetrahedral mesh topology with volume and edge constraints
- Real-time mesh topology updates after cutting operations
- Ground collision detection with damping
- Interactive compliance control

### Cutting System
- Intersection-based tetrahedral cutting
- Real-time mesh regeneration with proper surface triangulation
- Anchor point preservation during cutting operations
- Visual feedback with transformable cutter tool

## 🚀 Live Demo

- [**Original Demo**](demo.html) - Classic version with core functionality
- [**New Enhanced Demo**](newdemo.html) - Latest version with improved features and performance

## 🎮 Controls

### Mouse Controls
- **Left Click**: Primary interaction (deform, move cutter, place anchor, smooth)
- **Right Click**: Secondary interaction (rotate cutter in cut mode)
- **Both Buttons**: Scaling mode for cutter tool
- **Mouse Wheel**: Camera zoom
- **Middle Click + Drag**: Camera orbit

### Keyboard Shortcuts
- **C**: Execute cut operation (in cut mode)
- **R**: Restart simulation
- **M**: Cycle through interaction modes
- **A**: Clear all anchor points

### Interface Controls
- **Run/Stop**: Toggle physics simulation
- **Restart**: Reset to initial state
- **Squash**: Flatten the mesh for testing
- **Add Body**: Add additional soft body instances
- **Clear Anchors**: Remove all placed anchor points
- **Compliance Slider**: Adjust mesh stiffness

## 🔧 Technical Implementation

### Physics Engine
- **Position-Based Dynamics**: Stable constraint-based simulation
- **Tetrahedral Mesh**: Volume-preserving deformation
- **Edge Constraints**: Maintain mesh structure
- **Volume Constraints**: Preserve object volume

### Cutting Algorithm
```
1. Transform cutter mesh to world space
2. Find intersecting tetrahedra using AABB + geometric tests
3. Remove intersecting tetrahedra from mesh topology
4. Regenerate surface triangles with proper winding
5. Update edge lists and physics constraints
6. Apply velocity impulses to cut surfaces
```

### Mesh Processing
- **Surface Generation**: Automatic extraction of boundary triangles
- **Normal Computation**: Per-vertex normal averaging
- **Topology Updates**: Dynamic mesh modification support
- **Anchor System**: Fixed constraint management

## 🛠️ Technologies

- **Three.js**: 3D graphics and rendering
- **WebGL**: Hardware-accelerated graphics
- **JavaScript**: Core simulation logic
- **HTML5 Canvas**: Interactive viewport
- **Position-Based Dynamics**: Physics simulation method

## 📚 References

- [Position Based Dynamics](https://matthias-research.github.io/pages/publications/posBasedDyn.pdf) - Müller et al.
- [Real-time Cutting of Deformable Objects](https://www.cs.cmu.edu/~baraff/papers/sig03.pdf) - Bielser et al.
- [Tetrahedral Mesh Generation](https://www.tetgen.org/) - TetGen algorithm reference

## 🎨 Features in Detail

### Deform Mode
Interactive mesh deformation with:
- Closest vertex detection
- Smooth force application
- Realistic physics response
- Anchor point interaction

### Cut Mode
Advanced cutting system featuring:
- 3D cutter tool with transform controls
- Real-time intersection testing
- Topology-aware mesh splitting
- Surface regeneration

### Anchor System
Fixed point constraints with:
- Maximum 3 simultaneous anchors
- Visual anchor representation
- Drag and position adjustment
- Automatic restoration after cutting

### Smooth Mode
Mesh refinement tools including:
- Laplacian smoothing algorithm
- Localized application area
- Iterative smoothing passes
- Edge-preserving algorithms

## 🏗️ Architecture

The simulation consists of several key components:

- **SoftBody Class**: Core physics simulation object
- **MeshCutting Module**: Tetrahedral cutting algorithms
- **AnchorPoint Class**: Fixed constraint management
- **CutterObject Class**: Interactive cutting tool
- **Grabber System**: Mouse interaction handling

## 🎯 Performance

- **Real-time**: 60 FPS simulation at 120Hz physics steps
- **Scalable**: Adjustable substep count for performance tuning
- **Efficient**: Optimized constraint solving and mesh updates
- **Responsive**: Low-latency user interaction

## 🆕 New Enhanced Demo Features

The new demo (`newdemo.html`) includes additional improvements and optimizations:

- Enhanced visual interface and user experience
- Improved performance optimizations
- Additional interactive features
- Refined physics simulation parameters
- Better error handling and stability

## 🔮 Future Enhancements

- Multiple cutting tools
- Fracture patterns
- Material property variation
- Particle system integration
- Advanced smoothing algorithms
- Mesh subdivision techniques

---

*Built with passion for real-time physics simulation and computational geometry.*