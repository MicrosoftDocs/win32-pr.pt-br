---
description: O método IsPreroll determina se este exemplo é um exemplo de pré-roll. Um exemplo de pré-roll não deve ser exibido. Esse método implementa o método IMediaSample::IsPreroll.
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Método CMediaSample.IsPreroll (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634636"
---
# <a name="cmediasampleispreroll-method"></a>Método CMediaSample.IsPreroll

O `IsPreroll` método determina se este exemplo é um exemplo de pré-roll. Um exemplo de pré-roll não deve ser exibido. Esse método implementa o [**método IMediaSample::IsPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o exemplo for um exemplo de pré-roll e, caso contrário, S \_ FALSE.

## <a name="remarks"></a>Comentários

A [**variável de membro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




