---
title: Pesquisa síncrona
description: O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis forem encontrados.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783721"
---
# <a name="synchronous-searching"></a>Pesquisa síncrona

O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis forem encontrados. Para executar uma pesquisa síncrona, use um dos métodos de pesquisa síncrona da interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .

> [!Note]  
> As pesquisas síncronas levam pelo menos nove segundos para serem retornadas. O atraso é causado porque a mensagem de pesquisa UDP inicial deve ser enviada várias vezes. Essa duplicação conta com a inconfiabilidade do protocolo de rede subjacente. As pesquisas síncronas são melhores para interfaces de linha de comando. Elas não são recomendadas para interfaces gráficas do usuário.

 

O método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) pesquisa por dispositivo ou tipo de serviço. Esse método usa um URI de tipo como um parâmetro de entrada e retorna uma coleção de objetos de dispositivo. Um objeto de dispositivo representa um dispositivo individual.

Os exemplos a seguir demonstram como executar uma pesquisa síncrona para dispositivos em VBScript. Cada script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chamado com o URI de tipo (ID do serviço) para o tipo de dispositivo do player de mídia, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*. O método retorna uma coleção de objetos de dispositivo que corresponde aos dispositivos do player de mídia que foram encontrados. Para obter informações sobre como extrair objetos de dispositivo individuais de uma coleção, consulte [coleções de dispositivos retornadas por pesquisas síncronas](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Pesquisar dispositivos por tipo em VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Pesquisar dispositivo por tipo em C++

O exemplo a seguir demonstra uma pesquisa síncrona para dispositivos de player de mídia usando C++. A função usa um ponteiro para a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) como entrada e retorna o ponteiro de interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

O exemplo primeiro aloca um **BSTR** para representar o URI do tipo de dispositivo e, em seguida, passa isso para o método [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) . Ele também passa o endereço de um ponteiro [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local no buffer no qual o método, em seguida, armazena a coleção de dispositivos encontrados. Se a chamada de função for bem-sucedida, ela retornará o ponteiro para essa coleção.


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




