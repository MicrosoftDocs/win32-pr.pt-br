---
description: O método SetSink define um gerenciador de qualidade externo. Esse método implementa o método IQualityControl::SetSink.
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin.SetSink (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e94dc561e378ab526eee04f82e0f54a90889ee4396996d96d01f6c8da8c34d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108626"
---
# <a name="cbasepinsetsink-method"></a>Método CBasePin.SetSink

O `SetSink` método define um gerenciador de qualidade externo. Esse método implementa o [**método IQualityControl::SetSink.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piqc* 
</dt> <dd>

Ponteiro para a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) do gerenciador de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chame esse método para redirecionar mensagens de controle de qualidade para um gerenciador de qualidade externo. Para obter mais informações, consulte [Gerenciamento de controle de qualidade.](quality-control-management.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




