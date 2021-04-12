---
title: Explorando um dispositivo
description: Explorando um dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Gerenciador de Dispositivos, explorando dispositivos
- Gerenciador de Dispositivos, explorando dispositivos
- Guia de programação, explorando dispositivos
- aplicativos de área de trabalho, explorando dispositivos
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, explorando dispositivos
- explorando dispositivos
- armazenamentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364039"
---
# <a name="exploring-a-device"></a>Explorando um dispositivo

Explorar um dispositivo é semelhante a explorar uma unidade de disco. Todos os objetos em um dispositivo são chamados de *armazenamentos*. Um armazenamento pode ser um arquivo, uma pasta ou um objeto abstrato (como uma lista de reprodução) no dispositivo. Você deve examinar os atributos e metadados de um armazenamento (se houver suporte) para entender o tipo de armazenamento. Os armazenamentos são organizados hierarquicamente no dispositivo; cada armazenamento tem exatamente um pai e todos os armazenamentos acabaram em um único armazenamento de dispositivo raiz, normalmente denominado " \\ ".

As etapas a seguir descrevem como explorar um dispositivo:

1.  Obtenha a interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) de um dispositivo conforme descrito em [enumerando dispositivos](enumerating-devices.md).
2.  Chame [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) para recuperar uma interface [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) . Essa interface é usada para obter todos os objetos filho do armazenamento que retorna essa interface. Ao obter essa interface do dispositivo, como estamos aqui, ele manterá apenas um armazenamento: o armazenamento do dispositivo raiz.
3.  Chame [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) com uma contagem de 1 para recuperar a interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) para o armazenamento do dispositivo raiz. (Não é possível solicitar mais de um filho do dispositivo.)
4.  Examine todos os armazenamentos no dispositivo chamando recursivamente [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) e, em seguida, **IWMDMEnumStorage:: Next** para obter filhos de um armazenamento. Para ver se um armazenamento tem filhos para evitar as chamadas para **EnumStorage** e **Avançar**, você pode chamar [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para verificar os sinalizadores o \_ atributo de armazenamento WMDM \_ \_ tem \_ arquivos ou o \_ atributo de armazenamento WMDM \_ \_ tem \_ pastas. Para obter mais informações sobre como obter as propriedades de um armazenamento, consulte [obtendo e definindo metadados e atributos](getting-and-setting-metadata-and-attributes.md) e [obtendo e configurando metadados e atributos no aplicativo](getting-and-setting-metadata-and-attributes-in-the-application.md).

O Windows Media Gerenciador de Dispositivos não expõe um conjunto padrão de pastas para manter a mídia de um tipo específico (por exemplo, uma pasta "minhas listas de reprodução" para listas de reprodução). Cada dispositivo tem um sistema de arquivos exclusivo, e você terá que decidir um local apropriado para procurar ou enviar um arquivo específico.

> [!Note]  
> O Windows Explorer pode mostrar as pastas virtuais que não existem de fato no dispositivo. As pastas virtuais de exemplo são as pastas "mídia" e "dados" exibidas para dispositivos MTP. Essas pastas são criadas pelo Windows para tornar os downloads mais simples para os usuários finais; Eles não existem de fato no dispositivo. Seu aplicativo não deve depender de encontrar esses tipos de pastas gerais. Por outro lado, o Windows Explorer pode não mostrar algumas pastas ou objetos que existem no dispositivo (por exemplo, listas de reprodução).

 

O código de exemplo C++ a seguir demonstra a exploração recursiva de um dispositivo. Ele usa duas funções:

-   ExploreDevice, uma função inicial que recebe um ponteiro de dispositivo e Obtém um ponteiro para o enumerador raiz para esse dispositivo.
-   RecursiveExploreStorage, que é chamado para explorar um dispositivo recursivamente.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




