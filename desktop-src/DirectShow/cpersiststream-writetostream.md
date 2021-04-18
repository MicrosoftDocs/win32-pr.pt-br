---
description: Grava os dados do filtro em um determinado fluxo.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Método CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810241"
---
# <a name="cpersiststreamwritetostream-method"></a>Método CPersistStream. WriteToStream

Grava os dados do filtro em um determinado fluxo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStream* 
</dt> <dd>

Ponteiro para uma interface **IStream** que especifica o fluxo de destino dos dados do filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK. A classe derivada deve retornar um valor **HRESULT** válido.

## <a name="remarks"></a>Comentários

A versão padrão não grava nada; Ele pode ser substituído para gravar dados específicos para sua classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




