FROM mcr.microsoft.com/vscode/devcontainers/python

RUN pip3 --disable-pip-version-check --no-cache-dir install -U pip

COPY .devcontainer/requirements.txt /tmp/pip-tmp/
RUN pip3 --disable-pip-version-check --no-cache-dir install -r \
    /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp

COPY . /workspaces/clairvoyance/
RUN pip3 --disable-pip-version-check --no-cache-dir install -e "/workspaces/clairvoyance/[dev]"
