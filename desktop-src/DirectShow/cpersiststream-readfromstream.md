---
description: Lê os dados do filtro do fluxo determinado.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream.ReadFromStream (Pstream.h)
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
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073640"
---
# <a name="cpersiststreamreadfromstream-method"></a>Método CPersistStream.ReadFromStream

Lê os dados do filtro do fluxo determinado.

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

Ponteiro para uma interface **IStream** da qual os dados devem ser lidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK. A classe derivada deve retornar um valor **HRESULT** válido.

## <a name="remarks"></a>Comentários

A versão padrão não lê nada; ele pode ser substituído para ler dados específicos para sua classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




