FROM mcr.microsoft.com/dotnet/sdk:8.0

WORKDIR /app
COPY . .

# Install dotnet ef tool
RUN dotnet tool install -g dotnet-ef \
    && export PATH="$PATH:/root/.dotnet/tools" \
    && dotnet restore \
    && dotnet tool restore

ENV PATH="${PATH}:/root/.dotnet/tools"

CMD ["/bin/sh", "-c", "echo 'Temp image'"]
