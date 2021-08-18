---
description: Construtor CBasePin.CBasePin – Método do construtor.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Construtor CBasePin.CBasePin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbeead09843aa8bf66471caeaabbdb42ee8d97d01cdaa9a54809f35c437b52d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916896"
---
# <a name="cbasepincbasepin-constructor"></a>Construtor CBasePin.CBasePin

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração para o objeto . Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou esse pino.

</dd> <dt>

*Plock* 
</dt> <dd>

Ponteiro para um [**bloqueio CCritSec,**](ccritsec.md) usado para serializar alterações de estado. Pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método. Inicialize o valor como S \_ OK antes de criar o objeto . O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*Pname* 
</dt> <dd>

Cadeia de caracteres largos que contém o nome do pino. Para obter mais informações, [**consulte CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Membro da [**enumeração PIN \_ DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando a direção do pino.

</dd> </dl>

## <a name="remarks"></a>Comentários

A seção crítica especificada por *pLock* serializa o estado do pino, incluindo seu status de conexão, a escolha do alocador, o tipo de mídia e o status das operações de liberação. Não use esta seção crítica para serializar operações de streaming. Para obter mais informações, [consulte Data Flow no filtro Graph](data-flow-in-the-filter-graph.md).

Um filtro pode criar pinos em seu método de construtor, portanto, neste ponto, o ponteiro *pFilter* pode não se referir a um objeto válido. Armazene o ponteiro, mas não desreferencia-o enquanto estiver dentro do construtor do pino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




