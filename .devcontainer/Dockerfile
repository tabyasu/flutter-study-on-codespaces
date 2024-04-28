FROM dart

RUN apt-get update
RUN apt-get install -y curl git unzip xz-utils zip libglu1-mesa vim

RUN apt-get clean

# Git alias
RUN echo 'alias g="git"' >> ~/.bashrc
RUN echo 'alias ga="git add"' >> ~/.bashrc
RUN echo 'alias gd="git diff"' >> ~/.bashrc
RUN echo 'alias gb="git branch"' >> ~/.bashrc
RUN echo 'alias gba="git branch -av"' >> ~/.bashrc
RUN echo 'alias gc="git checkout"' >> ~/.bashrc
RUN echo 'alias gs="git status"' >> ~/.bashrc
RUN echo 'alias gr="git rebase"' >> ~/.bashrc
RUN echo 'alias glg="git log --oneline --graph"' >> ~/.bashrc
RUN echo 'alias gl="git log --oneline"' >> ~/.bashrc

RUN git clone https://github.com/flutter/flutter.git -b stable --depth 1 /flutter
ENV PATH="/flutter/bin:$PATH"
RUN flutter doctor
