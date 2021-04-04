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
# <a name="creating-the-device-finder"></a><span data-ttu-id="86abb-103">Criando o localizador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="86abb-103">Creating the Device Finder</span></span>

<span data-ttu-id="86abb-104">Os exemplos a seguir demonstram como criar uma instância do objeto localizador de dispositivo em C++, Visual Basic e VBScript.</span><span class="sxs-lookup"><span data-stu-id="86abb-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="86abb-105">As linguagens de script usam a ID programática (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) para identificar a classe do Device Finder.</span><span class="sxs-lookup"><span data-stu-id="86abb-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="86abb-106">O código C++ usa o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="86abb-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="86abb-107">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="86abb-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="86abb-108">Como este exemplo de C++ indica, o objeto de localizador de dispositivo expõe uma interface padrão, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="86abb-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="86abb-109">Os métodos dessa interface executam pesquisas de acordo com os critérios de pesquisa válidos para um dispositivo baseado em UPnP.</span><span class="sxs-lookup"><span data-stu-id="86abb-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="86abb-110">Essa interface é compatível com automação e, portanto, seus métodos podem ser chamados por código de script.</span><span class="sxs-lookup"><span data-stu-id="86abb-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="86abb-111">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="86abb-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




