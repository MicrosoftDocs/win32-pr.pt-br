---
description: Uma coleção é um objeto que contém um ou mais objetos. As coleções fornecem uma maneira eficiente de agrupar objetos semelhantes. Windows A WIA (Aquisição de Imagem) fornece coleções para os objetos DeviceInfo e Item.
ms.assetid: 26918f15-4ef9-425b-8565-e64fc2c72063
title: Usando objetos de coleção WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 58a4003394bcc163e9013914da6797a504ec16582b8bfac7915d7a49947c18f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813506"
---
# <a name="using-wia-collection-objects"></a>Usando objetos de coleção WIA

Uma coleção é um objeto que contém um ou mais objetos. As coleções fornecem uma maneira eficiente de agrupar objetos semelhantes. Windows A WIA (Aquisição de Imagem) fornece coleções para os [**objetos DeviceInfo**](-wia-deviceinfo.md) [**e Item.**](-wia-item.md)

Use coleções para enumerar os objetos que elas contêm. Por exemplo, o exemplo de VBScript a seguir obtém uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) do método [**Devices**](-wia-iwia-devices.md) e, em seguida, usa um **For... Cada** loop para iterar pela coleção:


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
> Os objetos de coleção wia são baseados em 0.

 

 

 



