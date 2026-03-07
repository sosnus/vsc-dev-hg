FROM codercom/code-server:latest

USER root

# install dependencies
RUN apt-get update && \
    apt-get install -y hugo git curl && \
    apt-get clean

USER coder

# install vscode extensions
RUN code-server --install-extension yzhang.markdown-all-in-one && \
    code-server --install-extension davidanson.vscode-markdownlint && \
    code-server --install-extension bierner.markdown-preview-github-styles && \
    code-server --install-extension budparr.language-hugo-vscode