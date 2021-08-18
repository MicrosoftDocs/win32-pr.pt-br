---
title: Criando o localizador de dispositivos
description: os exemplos a seguir demonstram como criar uma instância do objeto localizador de dispositivo em C++, Visual Basic e VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6af75ea5c267e156f89f1ae1e27a08928c097bbfea731f59add575397fbc00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137350"
---
# <a name="creating-the-device-finder"></a>Criando o localizador de dispositivos

os exemplos a seguir demonstram como criar uma instância do objeto localizador de dispositivo em C++, Visual Basic e VBScript. As linguagens de script usam a ID programática (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para identificar a classe do Device Finder. O código C++ usa o identificador de classe.

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



 

 




