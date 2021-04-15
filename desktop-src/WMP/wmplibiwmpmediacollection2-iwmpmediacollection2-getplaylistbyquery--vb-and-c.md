---
title: Método IWMPMediaCollection2 getPlaylistByQuery
description: O método getPlaylistByQuery retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia que correspondem às condições de consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- método getPlaylistByQuery Windows Media Player
- método getPlaylistByQuery Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747471"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>Método IWMPMediaCollection2:: getPlaylistByQuery

O `getPlaylistByQuery` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que correspondem às condições de consulta.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pQuery* \[ no\]
</dt> <dd>

A interface **WMPLib. IWMPQuery** que representa a consulta.

</dd> <dt>

*bstrMediaType* \[ no\]
</dt> <dd>

O **System. String** que é o tipo de mídia. Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".

</dd> <dt>

*bstrSortAttribute* \[ no\]
</dt> <dd>

O **System. String** que é o nome do atributo usado para classificação. Uma cadeia de caracteres de comprimento zero ("") significa que nenhuma classificação é aplicada.

</dd> <dt>

*fSortAscending* \[ no\]
</dt> <dd>

O valor **System. Boolean** que indica se a playlist deve ser classificada em ordem crescente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução recuperada.

## <a name="remarks"></a>Comentários

As consultas compostas usando **IWMPQuery** não diferenciam maiúsculas de minúsculas.

Quando a consulta composta especificada pelo parâmetro *pQuery* contém uma condição criada no atributo **MediaType** , essa condição é ignorada. O valor para o parâmetro *bstrMediaType* é sempre usado. Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *bstrMediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





