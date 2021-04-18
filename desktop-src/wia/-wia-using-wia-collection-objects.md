---
description: Uma coleção é um objeto que contém um ou mais objetos. As coleções fornecem uma maneira eficiente de agrupar objetos semelhantes. A aquisição de imagem do Windows (WIA) fornece coleções para os objetos DeviceInfo e item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Usando objetos de coleção WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22aa959547647070c733b8c3f81dd1181243bcb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788897"
---
# <a name="using-wia-collection-objects"></a><span data-ttu-id="84630-105">Usando objetos de coleção WIA</span><span class="sxs-lookup"><span data-stu-id="84630-105">Using WIA Collection Objects</span></span>

<span data-ttu-id="84630-106">Uma coleção é um objeto que contém um ou mais objetos.</span><span class="sxs-lookup"><span data-stu-id="84630-106">A collection is an object that contains one or more objects.</span></span> <span data-ttu-id="84630-107">As coleções fornecem uma maneira eficiente de agrupar objetos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="84630-107">Collections provide an efficient way of grouping similar objects.</span></span> <span data-ttu-id="84630-108">A aquisição de imagem do Windows (WIA) fornece coleções para os objetos [**DeviceInfo**](-wia-deviceinfo.md) e [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="84630-108">Windows Image Acquisition (WIA) provides collections for the [**DeviceInfo**](-wia-deviceinfo.md) and [**Item**](-wia-item.md) objects.</span></span>

<span data-ttu-id="84630-109">Use coleções para enumerar os objetos que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="84630-109">Use collections to enumerate the objects they contain.</span></span> <span data-ttu-id="84630-110">Por exemplo, o exemplo de VBScript a seguir obtém uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) do método [**Devices**](-wia-iwia-devices.md) e, em seguida, usa um **para... Cada** loop para iterar na coleção:</span><span class="sxs-lookup"><span data-stu-id="84630-110">For example, the following VBScript example obtains a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects from the [**Devices**](-wia-iwia-devices.md) method and then uses a **For...Each** loop to iterate through the collection:</span></span>


```
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ' Do something with the DeviceInfo object.
Next
</SCRIPT>
```



> [!Note]  
> <span data-ttu-id="84630-111">Os objetos da coleção WIA são baseados em 0.</span><span class="sxs-lookup"><span data-stu-id="84630-111">WIA collection objects are 0-based.</span></span>

 

 

 



