---
description: O método GetItemsFromUI do objeto Item exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Método Item.GetItemsFromUI
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
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669708"
---
# <a name="itemgetitemsfromui-method"></a>Método Item.GetItemsFromUI

O **método GetItemsFromUI** do [**objeto Item**](-wia-item.md) exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  acima (0)


</dt> <dd>

Padrão. \[em \] Especifica o comportamento da caixa de diálogo. Os valores válidos para esse parâmetro são os mesmos do parâmetro *lFlags* do [**método DeviceDlg.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)

</dd> </dl> </dd> <dt>

*Intenção* \[ Em\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  acima (0)


</dt> <dd>

Padrão. \[em \] Especifica que tipo de dados a imagem deve representar. Para ver uma lista de valores de intenção de imagem, consulte [**Constantes de intenção de imagem**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **ICollection**

Esse método retorna uma coleção de [**objetos Item**](-wia-item.md) que representam os itens selecionados pelo usuário. Se nenhum item for selecionado, a coleção será vazia.

## <a name="remarks"></a>Comentários

Para aplicativos Visual Basic Microsoft, adicione uma referência à "biblioteca de tipos Windows image acquisition 1.01".

Esse método se aplica somente a dispositivos (itens raiz). O método retorna uma coleção de [**objetos Item**](-wia-item.md) que representam as imagens ou clipes de áudio selecionados pelo usuário.

Se nenhum item for selecionado pelo usuário, o método retornará uma coleção vazia.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do **método GetItemsFromUI** para permitir que um usuário selecione imagens de uma caixa de diálogo.


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




