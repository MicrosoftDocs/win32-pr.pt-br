---
title: Método getAttributeName de IWMPMedia
description: O método getAttributeName retorna o nome do atributo correspondente ao índice especificado.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- Método getAttributeName Windows Media Player
- Método getAttributeName Windows Media Player interface , IWMPMedia
- Interface IWMPMedia Windows Media Player , método getAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad61be7a611eefc18f408f3f325a45b5f5952e81d53279f04f002f8d87dc2f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031056"
---
# <a name="iwmpmediagetattributename-method"></a>Método IWMPMedia::getAttributeName

O **método getAttributeName** retorna o nome do atributo correspondente ao índice especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o índice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.String** que é o nome do atributo.

## <a name="remarks"></a>Comentários

O nome do atributo retornado pode ser usado em conjunto com **getItemInfo** para recuperar o valor de um atributo nomeado específico.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [Referência de atributo](attribute-reference.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa getAttributeName** para preencher uma caixa de texto de várias linhas com o índice e o nome de cada atributo para o item de mídia atual. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
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

[**IWMPMedia.getItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





