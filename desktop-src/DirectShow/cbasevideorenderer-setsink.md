---
description: O método SetSink define o objeto IQualityControl que receberá mensagens de qualidade.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Método CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766328"
---
# <a name="cbasevideorenderersetsink-method"></a>Método CBaseVideoRenderer. SetSink

O `SetSink` método define o objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) que receberá mensagens de qualidade.

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

Ponteiro para o objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para o qual as notificações devem ser enviadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) no processador de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




