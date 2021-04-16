---
description: Layout das chaves do registro
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout das chaves do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758430"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="581ed-103">Layout das chaves do registro</span><span class="sxs-lookup"><span data-stu-id="581ed-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="581ed-104">Os filtros do DirectShow são registrados em dois locais:</span><span class="sxs-lookup"><span data-stu-id="581ed-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="581ed-105">A DLL que contém o filtro é registrada como o servidor COM do filtro.</span><span class="sxs-lookup"><span data-stu-id="581ed-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="581ed-106">Quando um aplicativo chama **CoCreateInstance** para criar o filtro, a biblioteca com do Microsoft Windows usa essa entrada de registro para localizar a dll.</span><span class="sxs-lookup"><span data-stu-id="581ed-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="581ed-107">Informações adicionais sobre o filtro podem ser registradas em uma categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="581ed-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="581ed-108">Essas informações permitem que o [enumerador de dispositivo do sistema](system-device-enumerator.md) e o [mapeador de filtro](filter-mapper.md) localizem o filtro.</span><span class="sxs-lookup"><span data-stu-id="581ed-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="581ed-109">Os filtros não são necessários para registrar as informações de filtro adicionais.</span><span class="sxs-lookup"><span data-stu-id="581ed-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="581ed-110">Desde que a DLL seja registrada como o servidor COM, um aplicativo pode criar o filtro e adicioná-lo a um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="581ed-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="581ed-111">No entanto, se você quiser que o filtro seja detectável pelo enumerador de dispositivo do sistema ou pelo mapeador de filtro, deverá registrar as informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="581ed-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="581ed-112">A entrada do registro para a DLL tem as seguintes chaves:</span><span class="sxs-lookup"><span data-stu-id="581ed-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="581ed-113">A entrada de registro para as informações de filtro tem as seguintes chaves:</span><span class="sxs-lookup"><span data-stu-id="581ed-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="581ed-114">é o GUID de uma categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="581ed-114">is the GUID of a filter category.</span></span> <span data-ttu-id="581ed-115">(Consulte [Filtrar categorias](filter-categories.md).) As informações do filtro são incluídas em um formato binário.</span><span class="sxs-lookup"><span data-stu-id="581ed-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="581ed-116">A interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) desempacota esses dados quando procura um filtro no registro.</span><span class="sxs-lookup"><span data-stu-id="581ed-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="581ed-117">Todos os GUIDs de categoria de filtro estão listados no registro na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="581ed-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



