---
description: Lê os dados do filtro a partir do fluxo especificado.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753747"
---
# <a name="cpersiststreamreadfromstream-method"></a>Método CPersistStream. ReadFromStream

Lê os dados do filtro a partir do fluxo especificado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStream* 
</dt> <dd>

Ponteiro para uma interface **IStream** da qual os dados serão lidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK. A classe derivada deve retornar um valor **HRESULT** válido.

## <a name="remarks"></a>Comentários

A versão padrão não lê nada; Ele pode ser substituído para ler dados específicos para sua classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




