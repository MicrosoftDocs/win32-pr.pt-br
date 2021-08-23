---
title: Pesquisa síncrona
description: O objeto Device Finder habilita pesquisas síncronas e assíncronas. As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis são encontrados.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f852957bed4bb73d9b31d0e26e099eb545b804953718d8cfd4e3cb44ea5f6c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999496"
---
# <a name="synchronous-searching"></a>Pesquisa síncrona

O objeto Device Finder habilita pesquisas síncronas e assíncronas. As pesquisas síncronas são concluídas e retornam o controle para o aplicativo de chamada somente depois que todos os dispositivos disponíveis são encontrados. Para executar uma pesquisa síncrona, use um dos métodos de pesquisa síncrona da interface [**IUPnPDevice Playback.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)

> [!Note]  
> As pesquisas síncronas levam pelo menos nove segundos para retornar. O atraso é causado porque a mensagem de pesquisa UDP inicial deve ser enviada várias vezes. Essa duplicação responde pela não confiabilidade do protocolo de rede subjacente. As pesquisas síncronas são melhores para interfaces de linha de comando. Eles não são recomendados para interfaces gráficas do usuário.

 

O [**método IUPnPDeviceType::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) pesquisa por tipo de dispositivo ou serviço. Esse método aceita um URI de tipo como um parâmetro de entrada e retorna uma coleção de objetos Device. Um objeto Device representa um dispositivo individual.

Os exemplos a seguir demonstram como executar uma pesquisa síncrona para dispositivos no VBScript. Cada script usa [**IUPnPDeviceType::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chamado com o tipo URI (ID de serviço) para o tipo de dispositivo do player de mídia, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*. O método retorna uma coleção de objetos Device que corresponde aos dispositivos de player de mídia que foram encontrados. Para obter informações sobre como extrair objetos de dispositivo individuais de uma coleção, consulte Coleções de [dispositivos retornadas por pesquisas síncronas](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Pesquisar dispositivos por tipo no VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Pesquisar dispositivo por tipo em C++

O exemplo a seguir demonstra uma pesquisa síncrona para dispositivos de player de mídia usando C++. A função leva um ponteiro para a interface [**IUPnPDevice Ltda**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) como entrada e retorna o ponteiro da interface [**IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)

O exemplo primeiro aloca um **BSTR** para representar o URI do tipo de dispositivo e, em seguida, passa isso para o [**método IUPnPDeviceType::FindByType.**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) Ele também passa o endereço de um ponteiro [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local no buffer no qual o método armazena a coleção de dispositivos encontrados. Se a chamada de função for bem-sucedida, ela retornará o ponteiro para essa coleção.


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



 

 




