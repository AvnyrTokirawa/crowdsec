ifeq ($(OS), Windows_NT)
	SHELL := pwsh.exe
	.SHELLFLAGS := -NoProfile -Command
	EXT = .exe
endif

# Go parameters
GO = go
GOBUILD = $(GO) build

BINARY_NAME = notification-sentinel$(EXT)

build: clean
	$(GOBUILD) $(LD_OPTS) $(BUILD_VENDOR_FLAGS) -o $(BINARY_NAME)

clean:
	@$(RM) $(BINARY_NAME) $(WIN_IGNORE_ERR)
