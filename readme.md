````markdown
# InfiniTune

Welcome to InfiniTune, a groundbreaking tool developed by students at GIKI, designed to automatically uncover optimal configurations for a DBMS's knobs. InfiniTune's unique feature includes a feedback loop mechanism, enabling the model to continuously learn and enhance its tuning capabilities as it interacts with databases. This not only streamlines the knob tuning process of a DBMS for individuals lacking specialized knowledge in database administration but also ensures that InfiniTune becomes progressively more proficient over time, refining its tuning process with each iteration.

## MacOS Quick Setup

### Prerequisites

- _Platform:_ macOS 13.2.1+
- _Python3:_ Ensure Python3 is installed on your system. If not, you can install it via Homebrew:
  ```bash
  brew update
  brew install python3
  ```
````

### Installation Steps

1. _Clone InfiniTune Repository:_

   ```bash
   git clone git@github.com:RaoEhsanElahi/InfiniTune.git
   ```

2. _Install PostgreSQL:_

   ```bash
   brew install postgresql
   ```

3. _Install Required Packages:_
   Navigate to the cloned InfiniTune repository directory and install the required Python packages:
   ```bash
   cd InfiniTune
   pip3 install -r requirements.txt
   ```

## Linux Quick Setup

### Prerequisites

- _Platform:_ Linux (any modern distribution)
- _Python3:_ Ensure Python3 is installed. If not, install it using your package manager:
  ```bash
  sudo apt update
  sudo apt install python3 python3-pip
  ```

### Installation Steps

1. _Clone InfiniTune Repository:_

   ```bash
   git clone git@github.com:RaoEhsanElahi/InfiniTune.git
   ```

2. _Install PostgreSQL:_

   ```bash
   sudo apt install postgresql postgresql-contrib
   ```

3. _Install Required Packages:_
   Navigate to the cloned InfiniTune repository directory and install the required Python packages:
   ```bash
   cd InfiniTune
   pip3 install -r requirements.txt
   ```

## Windows Quick Setup

### Prerequisites

- _Platform:_ Windows 10/11
- _Python3:_ Ensure Python3 is installed. You can download it from the [official Python website](https://www.python.org/downloads/).
- _Git Bash:_ Install Git Bash for running bash commands on Windows from [here](https://gitforwindows.org/).

### Installation Steps

1. _Clone InfiniTune Repository:_
   Open Git Bash and run:

   ```bash
   git clone git@github.com:RaoEhsanElahi/InfiniTune.git
   ```

2. _Install PostgreSQL:_
   Download and install PostgreSQL from the [official website](https://www.postgresql.org/download/windows/).

3. _Install Required Packages:_
   Open Command Prompt or Git Bash, navigate to the cloned InfiniTune repository directory, and install the required Python packages:
   ```bash
   cd InfiniTune
   pip install -r requirements.txt
   ```

## Getting Started

1. _Access PostgreSQL Configuration File Location:_

   Open a terminal (Command Prompt on Windows) and enter the PostgreSQL command-line interface:

   ```bash
   psql postgres
   ```

   Within the PostgreSQL command-line interface, run the following command to show the location of the configuration file:

   ```sql
   SHOW config_file;
   ```

   Copy the location of the PostgreSQL configuration file displayed.

2. _Configure InfiniTune:_

   Open the `config.py` file in the cloned InfiniTune repository directory and paste the copied PostgreSQL configuration file path in the `conf_path` variable:

   ```python
   conf_path = 'your_copied_configuration_file_path'
   ```

3. _Run InfiniTune:_

   Execute the `Evaluation.py` script:

   ```bash
   python3 Evaluation.py
   ```

   You will be prompted to enter your database name and related details such as threads and clients. After entering the required information, the model will tune your database, and the final knob configurations will be installed in your PostgreSQL.

Now you're all set to optimize your DBMS configurations effortlessly with InfiniTune! If you encounter any issues or have feedback, feel free to reach out.

```

```
