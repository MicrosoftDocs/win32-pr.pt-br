---
title: Método GetMarkerName de IWMPMedia
description: O método getmarcadorname retorna o nome do marcador no índice especificado.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- método GetMarkerName do Windows Media Player
- método getmarkname Windows Media Player, interface IWMPMedia
- Interface IWMPMedia do Windows Media Player, método getmarcadorname
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764603"
---
# <a name="iwmpmediagetmarkername-method"></a>Método IWMPMedia:: GetMarkerName

O método **Getmarcadorname** retorna o nome do marcador no índice especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MarkerNum* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o nome do marcador.

## <a name="remarks"></a>Comentários

Esse método retornará **NULL** se o marcador especificado não existir.

Alguns itens de mídia não contêm marcadores. Use **markerCount** para descobrir quantos marcadores estão no item de mídia atual.

Os números de índice de marcador começam em 1.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **Getmarcadorname** para preencher uma caixa de texto de várias linhas com os nomes dos marcadores no item de mídia atual. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





