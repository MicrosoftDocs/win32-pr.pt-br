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
# <a name="using-wia-collection-objects"></a>Usando objetos de coleção WIA

Uma coleção é um objeto que contém um ou mais objetos. As coleções fornecem uma maneira eficiente de agrupar objetos semelhantes. A aquisição de imagem do Windows (WIA) fornece coleções para os objetos [**DeviceInfo**](-wia-deviceinfo.md) e [**Item**](-wia-item.md) .

Use coleções para enumerar os objetos que eles contêm. Por exemplo, o exemplo de VBScript a seguir obtém uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) do método [**Devices**](-wia-iwia-devices.md) e, em seguida, usa um **para... Cada** loop para iterar na coleção:


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
> Os objetos da coleção WIA são baseados em 0.

 

 

 



