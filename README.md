# Minimal boost example with conan

If you are thinking, making a C++ project with boost is hard, I have a solution for you.

Here are the 7 steps you must follow:

1. clone this repository and cd into it

```git clone https://github.com/keszegrobert/cpp_boost_with_conan.git```

```cd cpp_boost_with_conan```

2. make a build directory which will hold the temporary build files

```mkdir build```

```cd build```

3. using the conanfile.txt build the requirements and put them into conan's cache. 
The path provided to the conan command should contain a conanfile.txt or conanfile.py

```conan install ../ --generator=virtualenv --build=missing```

4. activate the virtual environment created by the previous step. The paths will be set to contain everything needed for the development

On *nix systems use:

```source activate.sh```

On Windows* systems use:

```activate.bat```

5. generate the build files using the contents of the CMakeLists.txt file. The path provided to the cmake command should contain the CMakeLists.txt file

```cmake ..```

6. Build the generated solution

```cmake --build .```

7. Run the console application

```./helloboost```


