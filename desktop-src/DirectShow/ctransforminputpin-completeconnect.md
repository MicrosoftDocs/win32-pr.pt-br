---
description: O método CompleteConnect conclui uma conexão com outro PIN.
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
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768612"
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

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) . Ele chama o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) do filtro, que retorna s \_ OK na classe base. A classe derivada pode substituir o método **CTransformFilter:: CompleteConnect** para executar verificações adicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




