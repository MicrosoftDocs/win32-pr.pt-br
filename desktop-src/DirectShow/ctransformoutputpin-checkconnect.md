---
description: Método CTransformOutputPin. CheckConnect – o método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094944"
---
# <a name="ctransformoutputpincheckconnect-method"></a>Método CTransformOutputPin. CheckConnect

O `CheckConnect` método determina se uma conexão de PIN é adequada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Sucesso.<br/>                                 |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | O pino de entrada do filtro não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseOutputPin:: CheckConnect**](cbaseoutputpin-checkconnect.md) . Ele chama o método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) do filtro, que retorna s \_ OK na classe base. A classe derivada pode substituir o método **CTransformFilter:: CheckConnect** para executar verificações adicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




