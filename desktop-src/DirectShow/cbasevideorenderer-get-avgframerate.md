---
description: O \_ método Get AvgFrameRate calcula e recupera a taxa média de quadros obtida.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Método de CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751902"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>CBaseVideoRenderer. obter \_ método AvgFrameRate

O `get_AvgFrameRate` método calcula e recupera a taxa média de quadros obtida.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Ponteiro para o número de quadros por segundo desde o início do streaming.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualProp:: get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




