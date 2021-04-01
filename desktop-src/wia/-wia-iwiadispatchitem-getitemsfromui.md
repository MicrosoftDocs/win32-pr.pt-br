---
description: O método GetItemsFromUI do objeto item exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Método item. GetItemsFromUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090806"
---
# <a name="itemgetitemsfromui-method"></a>Método item. GetItemsFromUI

O método **GetItemsFromUI** do objeto [**Item**](-wia-item.md) exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  acima (0)


</dt> <dd>

Padrão. \[no \] especifica o comportamento da caixa de diálogo. Os valores válidos para esse parâmetro são os mesmos para o parâmetro *lFlags* do método [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .

</dd> </dl> </dd> <dt>

*Intenção* \[ no\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  acima (0)


</dt> <dd>

Padrão. \[em \] especifica o tipo de dados que a imagem deve representar. Para obter uma lista de valores de intenção de imagem, consulte [**constantes de objetivo de imagem**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **ICollection**

Esse método retorna uma coleção de objetos de [**Item**](-wia-item.md) que representam os itens selecionados pelo usuário. Se nenhum item for selecionado, a coleção estará vazia.

## <a name="remarks"></a>Comentários

Para aplicativos Microsoft Visual Basic, adicione uma referência a "biblioteca de tipos do Windows Image Acquisition 1, 1".

Esse método se aplica somente a dispositivos (itens raiz). O método retorna uma coleção de objetos de [**Item**](-wia-item.md) que representam as imagens ou os clipes de áudio selecionados pelo usuário.

Se nenhum item for selecionado pelo usuário, o método retornará uma coleção vazia.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método **GetItemsFromUI** para permitir que um usuário selecione imagens em uma caixa de diálogo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




