---
description: A propriedade Children do objeto item recupera uma coleção de objetos item. Os itens nesta coleção representam itens que são filhos diretos deste item na árvore hierárquica. Somente leitura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Propriedade Item. Children
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
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798298"
---
# <a name="itemchildren-property"></a>Propriedade Item. Children

A propriedade **Children** do objeto [**Item**](-wia-item.md) recupera uma coleção de objetos **Item** . Os itens nesta coleção representam itens que são filhos diretos deste item na árvore hierárquica. Somente leitura.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valor da propriedade

Variável que recebe os objetos.

## <a name="remarks"></a>Comentários

Use essa propriedade para navegar na árvore hierárquica de objetos de [**Item**](-wia-item.md) que representam um dispositivo, as pastas e os arquivos que residem no dispositivo.

A propriedade **Children** é uma coleção de objetos [**Item**](-wia-item.md) somente do nível diretamente abaixo desse objeto **Item** na árvore. Para navegar por níveis adicionais na árvore, use essa propriedade recursivamente.

Se o item não puder ou não tiver nenhum item filho, essa propriedade retornará uma coleção vazia.

> [!Note]  
> Esta coleção é baseada em 0.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da propriedade **Children** para recuperar e enumerar uma coleção de itens filho de um dispositivo. Se o dispositivo for uma câmera digital, a coleção normalmente conterá itens de pasta e de imagem. Se o dispositivo for um scanner, a coleção normalmente conterá itens que representam ambientes de verificação.


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




