---
description: 'O método SetSink define um Gerenciador de qualidade externo. Esse método implementa o método IQualityControl:: SetSink.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin. SetSink (Amfilter. h)
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
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748642"
---
# <a name="cbasepinsetsink-method"></a>Método CBasePin. SetSink

O `SetSink` método define um Gerenciador de qualidade externo. Esse método implementa o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .

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

Ponteiro para a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) do Gerenciador de qualidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Chame esse método para redirecionar mensagens de controle de qualidade para um Gerenciador de qualidade externo. Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




