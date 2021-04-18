---
description: O método RecordFrameLateness registra a hora em que a renderização ocorreu e coleta estatísticas para a página de propriedades.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Método CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789717"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>Método CBaseVideoRenderer. RecordFrameLateness

O `RecordFrameLateness` método registra a hora em que a renderização ocorreu e coleta estatísticas para a página de propriedades.

## <a name="syntax"></a>Sintaxe


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*trLate* 
</dt> <dd>

Valor que indica o quão tarde o exemplo estava além do tempo de vida, em unidades de tempo de referência.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tempo entre quadros, em unidades de tempo de referência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




