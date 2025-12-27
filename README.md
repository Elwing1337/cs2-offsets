ong faster than a2x

## Example Usage
```cpp
void Offsets::UpdateOffsets()
{
    std::string offsetsData, buttonsData, client_dllData;

    try
    {
        Web::Get("https://raw.githubusercontent.com/Elwing1337/cs2-offsets/refs/heads/main/offsets.json", offsetsData);
        Web::Get("https://raw.githubusercontent.com/Elwing1337/cs2-offsets/refs/heads/main/buttons.json", buttonsData);
        Web::Get("https://raw.githubusercontent.com/Elwing1337/cs2-offsets/refs/heads/main/client_dll.json", client_dllData);
    }
    catch (const std::exception& error)
    {
        throw std::runtime_error(std::string("Failed to fetch offsets: ") + error.what());
    }

    SetOffsets(offsetsData, buttonsData, client_dllData);
}
```

## CS2 Base
Still working on it hehe

## License

Licensed under the MIT license ([LICENSE](./LICENSE)).
