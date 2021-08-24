---
description: O método SetPreroll especifica se este exemplo é um exemplo de pré-roll. Um exemplo de pré-roll não deve ser exibido. Esse método implementa o método IMediaSample::SetPreroll.
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample.SetPreroll (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 410031ccf60e830c51615d267d3324167169c5de7960f79dc05b8c9e267463bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832096"
---
# <a name="cmediasamplesetpreroll-method"></a>Método CMediaSample.SetPreroll

O `SetPreroll` método especifica se este exemplo é um exemplo de pré-roll. Um exemplo de pré-roll não deve ser exibido. Esse método implementa o [**método IMediaSample::SetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Valor booliana que especifica se este é um exemplo de pré-roll. Se **TRUE**, este é um exemplo de pré-roll.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método atualiza a variável de membro [**CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica a propriedade preroll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




