---
description: Método CTransformInputPin. CompleteConnect – o método CompleteConnect conclui uma conexão com outro PIN.
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Método CTransformInputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085004"
---
# <a name="ctransforminputpincompleteconnect-method"></a>Método CTransformInputPin. CompleteConnect

O `CompleteConnect` método conclui uma conexão com outro PIN.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) . Ele chama o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) do filtro, que retorna s \_ OK na classe base. A classe derivada pode substituir o método **CTransformFilter:: CompleteConnect** para executar verificações adicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




