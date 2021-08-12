---
title: Propriedade de nome IWMPMedia
description: A propriedade name obtém ou define o nome do item de mídia.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- name property Windows Media Player
- propriedade name Windows Media Player , interface IWMPMedia
- Interface IWMPMedia Windows Media Player , propriedade name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46f4e99aaa7a05530a555cb51a6b1b10d511a342143f2be2bc7e029cc813cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568731"
---
# <a name="iwmpmedianame-property"></a>Propriedade IWMPMedia::name

A **propriedade** name obtém ou define o nome do item de mídia.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String** que é o nome do item de mídia.

## <a name="remarks"></a>Comentários

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa o nome** para alterar o nome do item de mídia atual. Uma caixa de texto permite que o usuário insira um novo nome e o nome é alterado em resposta ao evento Click de um botão. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





