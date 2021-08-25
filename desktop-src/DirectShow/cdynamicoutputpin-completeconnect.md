---
description: Método CDynamicOutputPin.CompleteConnect – o método CompleteConnect conclui uma conexão com um pino de entrada.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Método CDynamicOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d051bdd2757e37d3939616300ab0763ef2bebec727d48477f15a23e0f5178f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983166"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Método CDynamicOutputPin.CompleteConnect

O `CompleteConnect` método conclui uma conexão com um pino de entrada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa da falha.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseOutputPin::CompleteConnect.**](cbaseoutputpin-completeconnect.md) Para dar suporte a reconexões dinâmicas, esse método confirma o alocador se o filtro estiver ativo. Na classe base, as conexões podem ocorrer somente quando o filtro é interrompido, portanto, o alocador sempre é confirmado no [**método CBaseOutputPin::Active.**](cbaseoutputpin-active.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




