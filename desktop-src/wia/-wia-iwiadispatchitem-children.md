---
description: A propriedade Children do objeto Item recupera uma coleção de objetos Item. Os itens nesta coleção representam itens que são filhos diretos desse item na árvore hierárquica. Somente leitura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Propriedade Item.Children
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 72ce5119a10adc6a902d5a675d3ec116a3db1852a88e47ed852284cf44edf2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440725"
---
# <a name="itemchildren-property"></a>Propriedade Item.Children

A **propriedade Children** do objeto [**Item**](-wia-item.md) recupera uma coleção de **objetos Item.** Os itens nesta coleção representam itens que são filhos diretos desse item na árvore hierárquica. Somente leitura.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valor da propriedade

Variável que recebe os objetos .

## <a name="remarks"></a>Comentários

Use essa propriedade para navegar na árvore hierárquica [**de objetos Item**](-wia-item.md) que representam um dispositivo, as pastas e os arquivos que residem no dispositivo.

A **propriedade Children** é uma coleção de objetos [**Item**](-wia-item.md) somente do nível diretamente abaixo desse objeto **Item** na árvore. Para navegar em níveis mais baixos na árvore, use essa propriedade recursivamente.

Se o item não puder ou não tiver nenhum item filho, essa propriedade retornará uma coleção vazia.

> [!Note]  
> Essa coleção é baseada em 0.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da propriedade **Children** para recuperar e enumerar uma coleção dos itens filho de um dispositivo. Se o dispositivo for uma câmera digital, a coleção normalmente conterá itens de pasta e imagem. Se o dispositivo for um verificador, a coleção normalmente conterá itens que representam os colchões de verificação.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




