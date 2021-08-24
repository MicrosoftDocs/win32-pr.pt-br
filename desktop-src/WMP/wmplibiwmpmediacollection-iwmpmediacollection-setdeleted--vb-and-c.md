---
title: Método setDeleted IWMPMediaCollection
description: O método setDeleted move o item de mídia especificado para a pasta de itens excluídos. | Método setDeleted IWMPMediaCollection
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- Método setDeleted Windows Media Player
- método setDeleted Windows Media Player , interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player , método setDeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516d6aab26659fa2bba57bd961671b4dca0f92d367d5d9bb1f048e8fd19eb2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505946"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>Método IWMPMediaCollection::setDeleted

O `setDeleted` método move o item de mídia especificado para a pasta de itens excluídos.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItem* \[ Em\]
</dt> <dd>

Uma interface **WMPLib.IWMPMedia** para o item a ser movido.

</dd> <dt>

*varfIsDeleted* \[ Em\]
</dt> <dd>

Um **valor System.Boolean** que especifica se o item deve ser movido para a pasta de itens excluídos. Esse valor sempre deve ser **true.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não remove arquivos do computador do usuário, apenas os move para a pasta de itens excluídos.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir `setDeleted` usa para mover um item de mídia específico para a pasta de itens excluídos. O **método isDeleted** primeiro testa se o item já foi excluído. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
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
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





