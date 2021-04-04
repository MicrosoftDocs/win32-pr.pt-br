---
title: Criando o localizador de dispositivos
description: Os exemplos a seguir demonstram como criar uma instância do objeto localizador de dispositivo em C++, Visual Basic e VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822883"
---
# <a name="creating-the-device-finder"></a>Criando o localizador de dispositivos

Os exemplos a seguir demonstram como criar uma instância do objeto localizador de dispositivo em C++, Visual Basic e VBScript. As linguagens de script usam a ID programática (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para identificar a classe do Device Finder. O código C++ usa o identificador de classe.

## <a name="c-example"></a>Exemplo de C++


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Como este exemplo de C++ indica, o objeto de localizador de dispositivo expõe uma interface padrão, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). Os métodos dessa interface executam pesquisas de acordo com os critérios de pesquisa válidos para um dispositivo baseado em UPnP. Essa interface é compatível com automação e, portanto, seus métodos podem ser chamados por código de script.

## <a name="vbscript-example"></a>Exemplo de VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




