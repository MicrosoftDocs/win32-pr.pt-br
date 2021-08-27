---
description: Método CTransformOutputPin.CheckConnect – o método CheckConnect determina se uma conexão de pino é adequada.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: 2b85c2197cf65465441387ecc661af71e0ddfa7ca912c3296ddee543d11c4784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086986"
---
# <a name="ctransformoutputpincheckconnect-method"></a>Método CTransformOutputPin.CheckConnect

O `CheckConnect` método determina se uma conexão de pino é adequada.

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

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                 |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | O pino de entrada do filtro não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseOutputPin::CheckConnect.**](cbaseoutputpin-checkconnect.md) Ele chama o método [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) do filtro, que retorna S \_ OK na classe base. A classe derivada pode substituir o **método CTransformFilter::CheckConnect** para executar verificações adicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




