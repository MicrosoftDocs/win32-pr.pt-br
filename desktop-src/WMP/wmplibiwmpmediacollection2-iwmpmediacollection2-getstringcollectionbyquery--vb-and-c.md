---
title: Método IWMPMediaCollection2 getStringCollectionByQuery
description: O método getStringCollectionByQuery retorna uma interface IWMPStringCollection que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- Windows Media Player do método getStringCollectionByQuery
- método getStringCollectionByQuery Windows Media Player, interface IWMPMediaCollection2
- Windows Media Player de interface IWMPMediaCollection2, método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054dd5b76cb6dcf3e6cb29ba624cd1f5c0f281d69c4b2b5e5125f5de9b4e7b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745964"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>Método IWMPMediaCollection2:: getStringCollectionByQuery

O `getStringCollectionByQuery` método retorna uma interface **IWMPStringCollection** que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrattribute* \[ no\]
</dt> <dd>

O **System. String** que é o nome do atributo.

</dd> <dt>

*pQuery* \[ no\]
</dt> <dd>

A interface **WMPLib. IWMPQuery** que é a consulta que define as condições usadas para recuperar a coleção de cadeias de caracteres.

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

O valor **System. Boolean** que indica se o conjunto de valores de cadeia de caracteres deve ser classificado em ordem crescente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib. IWMPStringCollection** para o conjunto recuperado de valores de cadeia de caracteres.

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

[**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





