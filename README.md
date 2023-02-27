# RSA-like-cryptosystem

This repository contains a project that was developed for a software engineering degree. The project is based on the mathematical article titled "An efficient and secure RSA-like cryptosystem exploiting R´edei rational functions over conics". The abstract of the article describes a novel RSA-like scheme that is faster and more secure than the classic RSA algorithm in broadcast applications.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- A modern C++ compiler.
- Git
- Visual Studio Code or any other C++ development environment.
- To use GMP library please install the library from http://rstudio-pubs-static.s3.amazonaws.com/493124_a46782f9253a4b8193595b6b2a037d58.html#15_on_ubuntu
- GMP library official site - https://gmplib.org

### Installing

1. Clone the repository to your local machine using Git.

$ git clone https://github.com/AsafYus/RSA-like-cryptosystem.git

2. Open the project in Visual Studio Code or your preferred C++ development environment.

3. Build and run the application.


### Project Overview
The project aims to implement an RSA-like cryptosystem that is more efficient than the original RSA algorithm. The original RSA algorithm is based on integer factorization problem and discrete logarithm problem, and the processes of encryption and decryption require a higher running time. In contrast, the proposed cryptosystem uses Rédei rational functions based on the conic equation, which offers a one-to-one correspondence between two mathematical sets. Our proposed cryptosystem becomes two times faster than the original textbook RSA cryptosystem by involving the lowest number of modular inversions with respect to the original textbook RSA. Our proposed cryptosystem affords higher security in broadcast applications and an equal level of security in a one-to-one communication.

### Project Details
The project began with an in-depth study of the RSA algorithm, including the reading and internalization of the entire official patent of the inventors: Ronald L. Rivest, Adi Shamir, Leonard M. Adleman. The project then covered the historical overview of RSA, security of RSA in relation to factoring and attacks on RSA, conic equations usage in cryptography, and the use of Pell's equation.

The project then presented the parametrization in our scheme, which allowed us to define a bijection between a conic that we use and the set of parameters. After the explanation of all the parametrization, we moved to the algorithm given in the mathematical article. Finally, we presented the expected results of our project objective along with the presentation of the testing plan.

The project was written in C++ using the GMP library, which allowed us to use its tools designed for very large numbers, such as mpz_urandomb and mpz_probab_prime_p.

### Conclusion
In conclusion, during the experiment stage, we tested the RSA-like cryptosystem with various parameter values and compared its performance to the original RSA. We found that the decryption time of the RSA-like cryptosystem is heavily affected by the size of the parameters 𝑝 and 𝑞 - the larger these parameters, the longer the decryption time. After careful consideration, we concluded that the original RSA has a faster decryption time than the RSA-like cryptosystem. Additionally, the number of iterations in the RSA-like cryptosystem affects its running time, and this number cannot be reduced as it depends on the value of 𝑒.

We also identified some weak points in the encryption and decryption procedures. The calculation of the factorial of large numbers is time-consuming and there is no shortcut to calculate it. The calculation of the factorial appears in Rédei rational functions that are used in the encryption and decryption procedures. Furthermore, in every one iteration of the decryption process, the original RSA only requires one multiplication operation as part of the raising to the power, while the RSA-like cryptosystem needs to calculate five complicated operations to be an alternative to the raising to the power of the original RSA.

Based on the time results of hundreds of running tests of the original RSA and RSA-like cryptosystem, we found that our assumption could not be achieved.


