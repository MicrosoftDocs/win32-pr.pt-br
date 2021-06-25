---
title: Palavras-chave dinâmicas do firewall
description: Use as APIs de palavras-chave dinâmicas do firewall para gerenciar endereços de palavra-chave dinâmicos Microsoft Defender Firewall.
keywords:
- Palavras-chave dinâmicas do firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: 15e35f26b72ed8d685e8302f6222836507e5c6a3
ms.sourcegitcommit: ae8c320a757558262167a4f4e385235b8d89035c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112765530"
---
# <a name="firewall-dynamic-keywords"></a>Palavras-chave dinâmicas do firewall

Use as APIs de palavras-chave dinâmicas do firewall para gerenciar endereços *de palavra-chave* dinâmicos [no Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security). Um endereço de palavra-chave dinâmico é usado para criar um conjunto de endereços IP aos quais uma ou mais regras de firewall podem se referir. Endereços de palavra-chave dinâmicos são suportados por IPv4 e IPv6.

> [!NOTE]
> Para conteúdo de referência de API para as APIs introduzidas neste tópico, consulte [Referência de palavras-chave dinâmicas do firewall](firewall-dynamic-keywords-reference.md).

## <a name="operations-on-dynamic-keyword-addresses"></a>Operações em endereços de palavra-chave dinâmicos

Com as APIs de palavras-chave dinâmicas do Firewall, você pode executar as operações a seguir.

* Adicionar endereços de palavra-chave dinâmicos
* Excluir endereços de palavra-chave dinâmicos
* Enumerar endereços de palavra-chave dinâmicos por ID ou por tipo
* Atualizar endereços de palavra-chave dinâmicos
* Assinar e manipular notificações de alteração de endereço de palavra-chave dinâmica

Há exemplos de código para todas essas operações posteriormente neste tópico.

Depois de adicionar um endereço de palavra-chave dinâmico, ele persiste entre reinicializações. Você deve excluir um endereço de palavra-chave dinâmico depois de terminar com o objeto .

Há duas classes de endereços de palavra-chave dinâmicos, conforme descrito nas próximas duas seções.

## <a name="autoresolve-dynamic-keyword-addresses"></a>Endereços de palavra-chave dinâmicos autoResolve

O primeiro tipo é *AutoResolve,* em que o campo de palavra-chave representa um nome resolvível e os endereços IP não são definidos após a criação. 

Esses objetos destinam-se a ter seus endereços IP resolvidos automaticamente. Ou seja, não por meio de um administrador no momento da criação do objeto; nem por meio do sistema operacional em si. Um componente fora do serviço de firewall deve fazer a resolução de endereço IP para esses objetos e atualizá-los adequadamente. A implementação desse componente está fora do escopo desse conteúdo.

Um endereço de palavra-chave dinâmico é indicado como *AutoResolve* definindo o sinalizador **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** no objeto ao chamar a [**função FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) O *campo* de palavra-chave deve ser usado para representar o valor que está sendo resolvido, ou seja, um &mdash; FQDN (nome de domínio totalmente qualificado) ou nome de host. O *campo* de endereços deve inicialmente ser NULL para esses objetos. Esses objetos não terão seus endereços IP persistentes entre os ciclos de inicialização e você deverá reavalidar/preencher seus endereços durante o próximo ciclo de inicialização.

> [!NOTE]
> Objetos de endereço de palavra-chave dinâmica AutoResolve disparam notificações [**em FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) e [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), mas não [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="non-autoresolve-dynamic-keyword-addresses"></a>Endereços de palavra-chave dinâmicos não AutoResolve

O segundo tipo é *não AutoResolve,* em que o campo de palavra-chave é qualquer cadeia de caracteres e os endereços são definidos no momento da criação. 

Esses objetos são usados para armazenar um conjunto de endereços IP, sub-redes ou intervalos. O *campo de* palavra-chave aqui é usado para conveniência de gerenciamento e pode ser definido como qualquer cadeia de caracteres. O *campo de* endereços deve ser não NULL após a criação. Os endereços para esses objetos são persistentes entre reinicializações.

> [!NOTE]
> Objetos de endereço de palavra-chave dinâmico não AutoResolve disparam notificações [**em FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)e [**também FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="more-about-dynamic-keyword-addresses"></a>Mais sobre endereços de palavra-chave dinâmicos 

Todos os endereços de palavra-chave dinâmicos devem ter um [**identificador GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) exclusivo para representá-los.

A API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) fornece notificações a um cliente quando os endereços de palavra-chave dinâmicos mudam. Não há nenhum payload entregue ao cliente que descreve exatamente o que mudou no sistema. Se você precisar saber quais objetos foram alterados, consulte o estado atual dos objetos no sistema usando as APIs [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) ou [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) Você pode usar os vários sinalizadores para solicitar notificações apenas para um subconjunto de objetos. Se você não usar sinalizadores, as notificações de alteração serão entregues para todos os objetos.

Uma regra de firewall pode usar endereços de palavra-chave dinâmicos em vez de definir explicitamente endereços IP para sua condição de endereço remoto. Uma regra de firewall pode usar endereços de palavra-chave dinâmicos e intervalos de endereços remotos definidos estaticamente. Um único objeto de endereço de palavra-chave dinâmica pode ser rea usado em várias regras de firewall. Se uma regra de firewall não tiver endereços remotos configurados (ou seja, configurados apenas com objetos AutoResolve que ainda não foram resolvidos), a regra não será imposta. Além disso, se uma regra usar vários endereços de palavra-chave dinâmicos, a regra será imposta para todos os endereços que estão resolvidos no momento, mesmo se houver outros objetos que ainda não foram resolvidos. Quando um endereço de palavra-chave dinâmico for atualizado, todos os objetos de regra associados também terão seus endereços remotos atualizados.

O sistema operacional em si não impõe nenhuma dependência entre uma regra e um endereço de palavra-chave dinâmico. Isso significa que qualquer objeto pode ser criado primeiro, a regra pode referenciar IDs de endereço de palavra-chave dinâmicas que ainda não existem (nesse caso, a regra não &mdash; será imposta). Além disso, você pode excluir um endereço de palavra-chave dinâmico mesmo que ele seja usado por uma regra de firewall. Este tópico descreve como um administrador pode configurar regras para usar o endereço de palavra-chave dinâmico.

## <a name="code-examples"></a>Exemplos de código

Para experimentar cada um desses exemplos de código, primeiro Visual Studio e criar um novo projeto com base no modelo de projeto **aplicativo** de console. Você pode simplesmente substituir o conteúdo de `main.cpp` pela listagem de código.

A maioria dos exemplos de código usa o [WIL (Bibliotecas de Implementação do Windows).](https://github.com/Microsoft/wil) Uma maneira conveniente de instalar o WIL é  acessar o Visual Studio, clicar em Projeto Gerenciar Pacotes NuGet... Procurar , digitar ou colar \>  \>  **Microsoft.Windows.ImplementationLibrary**  na caixa de pesquisa, selecionar o item nos resultados da pesquisa e, em seguida, clicar em Instalar para instalar o pacote para esse projeto.

> [!NOTE]
> Os tipos de ponteiro para as funções gratuitas do NetFw são publicados por meio de , mas uma biblioteca `NetFw.h` de link estático não é publicada. Use o padrão GetProcAddress [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)para chamar essas funções, conforme / [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mostrado nesses exemplos de código.

### <a name="add-a-dynamic-keyword-address"></a>Adicionar um endereço de palavra-chave dinâmico

Este exemplo mostra como usar a [**função FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a>Excluir um endereço de palavra-chave dinâmico

Este exemplo mostra como usar a [**função FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a>Enumerar e liberar endereços de palavra-chave dinâmicos por ID

Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a>Enumerar e liberar endereços de palavra-chave dinâmicos por tipo

Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a>Atualizar endereços de palavra-chave dinâmicos

Este exemplo mostra como usar a [**função FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a>Assinar e manipular notificações de alteração de endereço de palavra-chave dinâmica

Este exemplo mostra como usar as funções [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) e [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) e o [**retorno FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) retorno de chamada.

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de palavras-chave dinâmicas do firewall](firewall-dynamic-keywords-reference.md)
