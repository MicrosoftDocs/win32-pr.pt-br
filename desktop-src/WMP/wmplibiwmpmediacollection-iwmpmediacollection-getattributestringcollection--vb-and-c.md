---
title: Método getAttributeStringCollection de IWMPMediaCollection
description: O método getAttributeStringCollection retorna uma interface IWMPStringCollection que representa o conjunto de todos os valores para um atributo especificado dentro de um tipo de mídia.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Método getAttributeStringCollection Windows Media Player
- Método getAttributeStringCollection Windows Media Player interface , IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player método , getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508630ee8a377e1542f823c1afb21521206369aa3ce489c58afae47efa268880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331938"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>Método IWMPMediaCollection::getAttributeStringCollection

O **método getAttributeStringCollection** retorna uma interface **IWMPStringCollection** que representa o conjunto de todos os valores para um atributo especificado dentro de um tipo de mídia.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrAttribute* \[ Em\]
</dt> <dd>

Um **System.String** que é o atributo para o qual os valores são recuperados.

</dd> <dt>

*bstrMediaType* \[ Em\]
</dt> <dd>

Um **System.String** que é o tipo de mídia para o qual os valores são recuperados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib.IWMPStringCollection** para os valores recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [Referência de atributo](attribute-reference.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa getAttributeStringCollection** para exibir uma lista de valores que correspondem a um atributo específico para itens de áudio na coleção de mídias. Uma caixa de listagem permite que o usuário selecione um atributo, como Artist, Genre ou Album e uma caixa de texto de várias linhas exibe o resultado. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

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

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





