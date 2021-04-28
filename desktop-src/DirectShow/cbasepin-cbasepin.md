---
description: Construtor de CBasePin. CBasePin-método de construtor.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Construtor CBasePin. CBasePin (Amfilter. h)
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
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099424"
---
# <a name="cbasepincbasepin-constructor"></a>Construtor CBasePin. CBasePin

Método de construtor.

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

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou este pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado. Pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método. Inicialize o valor para S \_ OK antes de criar o objeto. O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres largos contendo o nome do PIN. Para obter mais informações, consulte [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Membro da enumeração [**de \_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando a direção do PIN.

</dd> </dl>

## <a name="remarks"></a>Comentários

A seção crítica especificada por *pLock* serializa o estado do PIN, incluindo seu status de conexão, a escolha do alocador, o tipo de mídia e o status das operações de liberação. Não use essa seção crítica para serializar operações de streaming. Para obter mais informações, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).

Um filtro pode criar Pins em seu método construtor, portanto, neste ponto, o ponteiro *pFilter* pode não se referir a um objeto válido. Armazene o ponteiro, mas não o referencie enquanto estiver dentro do construtor do PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




