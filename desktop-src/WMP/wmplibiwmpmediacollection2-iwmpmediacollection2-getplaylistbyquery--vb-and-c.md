---
title: Método IWMPMediaCollection2 getPlaylistByQuery
description: O método getPlaylistByQuery retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia que correspondem às condições de consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Windows Media Player do método getPlaylistByQuery
- método getPlaylistByQuery Windows Media Player, interface IWMPMediaCollection2
- Windows Media Player de interface IWMPMediaCollection2, método getPlaylistByQuery
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
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053574"
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

## <a name="return-value"></a>Valor retornado

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

 

 





