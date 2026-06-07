# DataStructure-Visualizer 🎨

Interactive Data Structure Visualization Tool in C++ - Make Learning Data Structures Fun!

![License](https://img.shields.io/badge/license-MIT-green)
![Language](https://img.shields.io/badge/language-C%2B%2B17-blue)
![Status](https://img.shields.io/badge/status-Active-brightgreen)

## 📖 Overview

**DataStructure-Visualizer** is an educational tool that helps students understand data structures by visualizing their operations step-by-step. Instead of just seeing code, you can now see how your data structures actually work!

### Features ✨

- 🔗 **Linked List Visualization** - Insert, delete, traverse operations
- 🌳 **Binary Tree Visualization** - Tree traversal and balancing (coming soon)
- 📊 **Graph Visualization** - DFS, BFS, and pathfinding algorithms (coming soon)
- 📈 **Heap Visualization** - Min/Max heap operations (coming soon)
- 🎯 **Stack & Queue** - FIFO and LIFO operations (coming soon)
- 📁 **HTML/SVG Output** - Beautiful, interactive visualizations
- 🧪 **Unit Tests** - Comprehensive test coverage
- ✅ **GitHub Actions CI/CD** - Automated testing and building

## 🎯 Quick Start

### Prerequisites
- C++17 or later
- CMake 3.15+
- Git
- Linux/Mac/Windows (with appropriate build tools)

### Installation & Running

```bash
# Clone the repository
git clone https://github.com/yangzihao11/DataStructure-Visualizer.git
cd DataStructure-Visualizer

# Create build directory
mkdir build
cd build

# Build the project
cmake ..
make

# Run tests
./DataStructureVisualizerTests

# Run the demo
./linked_list_demo

# View the generated visualization
# Open "linked_list_output.svg" in your web browser
```

## 📚 Usage Example

### Basic LinkedList Usage

```cpp
#include "LinkedList.h"
#include "SVGVisualizer.h"

int main() {
    // Create a linked list of integers
    LinkedList<int> list;
    
    // Add elements
    list.insertAtEnd(5);
    list.insertAtEnd(3);
    list.insertAtEnd(8);
    list.insertAtEnd(1);
    
    // Print to console
    list.print();  // Output: LinkedList: 5 -> 3 -> 8 -> 1 -> NULL
    
    // Generate SVG visualization
    SVGVisualizer visualizer;
    visualizer.visualizeLinkedList(list, "my_list.svg");
    
    // The SVG file can be opened in any web browser!
    return 0;
}
```

### More Operations

```cpp
// Insert at specific position
list.insertAtPosition(7, 2);  // Insert 7 at position 2

// Delete element
list.deleteAtPosition(0);      // Remove first element

// Search for element
int pos = list.search(8);      // Returns position or -1

// Get element at position
int value;
list.getAt(1, value);          // Get value at position 1

// List statistics
int size = list.getSize();     // Get size
bool empty = list.isEmpty();   // Check if empty

// Clear the list
list.clear();                  // Remove all elements
```

## 📁 Project Structure

```
DataStructure-Visualizer/
├── CMakeLists.txt              # Build configuration
├── README.md                   # This file
├── CONTRIBUTING.md             # Contribution guidelines
├── LICENSE                     # MIT License
├── .gitignore
│
├── include/                    # Header files
│   ├── LinkedList.h            # LinkedList template class
│   └── SVGVisualizer.h         # SVG visualization engine
│
├── src/                        # Implementation files
│   ├── LinkedList.cpp          # Template instantiations
│   └── SVGVisualizer.cpp       # Visualization implementation
│
├── examples/                   # Example programs
│   └── linked_list_demo.cpp    # Demo with various operations
│
├── tests/                      # Unit tests
│   └── LinkedListTest.cpp      # LinkedList tests
│
└── .github/workflows/          # CI/CD pipelines
    └── build.yml               # Automated testing
```

## 🧪 Running Tests

```bash
cd build
ctest --output-on-failure
```

## 🎓 Learning Path

This is perfect for students like you:

### Phase 1: Understand the Basics (Week 1)
- [ ] Review the LinkedList implementation
- [ ] Understand how nodes are linked
- [ ] Learn basic operations: insert, delete, search
- [ ] Run the demo program

### Phase 2: Practice & Extend (Week 2-3)
- [ ] Modify the demo to create your own test cases
- [ ] Write additional test cases
- [ ] Generate visualizations for different scenarios
- [ ] Understand the SVG generation

### Phase 3: Contribute (Week 4+)
- [ ] Implement Binary Tree visualization
- [ ] Add Stack and Queue implementations
- [ ] Create more comprehensive tests
- [ ] Improve documentation

## 📚 Key Concepts

### LinkedList Operations Complexity

| Operation | Time Complexity | Space |
|-----------|-----------------|-------|
| Insert at beginning | O(1) | O(1) |
| Insert at end | O(n) | O(1) |
| Insert at position | O(n) | O(1) |
| Delete at position | O(n) | O(1) |
| Search | O(n) | O(1) |
| Access | O(n) | O(1) |

### Why Visualize?

📊 **Benefits of Visual Learning:**
- See how data structures actually change
- Understand algorithm steps intuitively
- Identify edge cases more easily
- Better retention of concepts
- More engaging than just code

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

**Easy ways to start:**
1. 🐛 **Report bugs** - Found an issue? Create an Issue
2. 📝 **Improve docs** - Clarify confusing parts
3. ✨ **Add features** - Implement new data structures
4. 🧪 **Write tests** - Increase test coverage
5. 🎨 **Improve visualization** - Make SVG outputs prettier

### Contribution Workflow

```bash
# 1. Fork the repository

# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/DataStructure-Visualizer.git
cd DataStructure-Visualizer

# 3. Create a feature branch
git checkout -b feature/amazing-feature

# 4. Make changes and commit
git add .
git commit -m "feat: add amazing feature"

# 5. Push to your fork
git push origin feature/amazing-feature

# 6. Create a Pull Request on GitHub
```

## 📊 Project Statistics

- **Lines of Code**: ~500+ (growing!)
- **Test Coverage**: Comprehensive unit tests
- **Documentation**: Detailed comments and guides
- **Supported C++ Standard**: C++17+

## 🚀 Roadmap

### Current Status ✅
- [x] Linked List implementation
- [x] SVG visualization engine
- [x] Comprehensive unit tests
- [x] GitHub Actions CI/CD
- [x] Contributing guidelines

### Next Steps (Contributions Welcome!) 🎯
- [ ] **Binary Tree Visualization** (Medium difficulty)
- [ ] **Stack & Queue Visualization** (Easy)
- [ ] **Graph Algorithms** (Hard)
- [ ] **Heap Visualization** (Medium)
- [ ] **Web Dashboard** (Very Hard)
- [ ] **Performance Benchmarks**
- [ ] **More Data Structures** (Trie, HashTable, etc.)

## 💡 For Students (Like You!)

### For Exams & Interviews
- Use visualizations to understand algorithms deeply
- Generate diagrams for study materials
- Trace through examples step-by-step

### For Your Resume
- This is a **real open-source project**
- Good portfolio item for internships/jobs
- Shows understanding of data structures AND software engineering

### For Learning
- **Read quality code** - This codebase follows best practices
- **Write tests** - Learn test-driven development
- **Contribute** - Gain real collaboration experience

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details

This means you can:
- ✅ Use it for personal projects
- ✅ Use it for commercial purposes
- ✅ Modify and distribute
- ✅ Include in your resume/portfolio

Just keep the license notice!

## 🙌 Acknowledgments

- Inspired by VisuAlgo and other visualization tools
- Built for the learning community
- Special thanks to all future contributors!

## 📮 Contact & Support

- **GitHub Issues** - 🐛 Report bugs or 💡 request features
- **GitHub Discussions** - 💬 Ask questions
- **Pull Requests** - 📤 Submit contributions

## 🌟 Show Your Support

If you find this helpful:
- ⭐ **Star the repository** - Helps others discover it
- 🔔 **Watch for updates** - Don't miss new features
- 📢 **Share with classmates** - Help them learn too
- 🤝 **Contribute** - Make it even better!

---

**Made with ❤️ for students learning data structures**

Last Updated: 2026
Actively Maintained ✨
