---
description: Método CSourceSeeking.GetDuration – o método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking::GetDuration.
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Método CSourceSeeking.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8520b39ca62d70152b544e8ae2f146a237c388d93e4786bb13371ad223fa73f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084036"
---
# <a name="csourceseekinggetduration-method"></a>Método CSourceSeeking.GetDuration

O `GetDuration` método recupera a duração do fluxo. Esse método implementa o [**método IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDuration* 
</dt> <dd>

Ponteiro para uma variável que recebe a duração, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | **Valor do** ponteiro NULL<br/> |



 

## <a name="remarks"></a>Comentários

A duração é especificada pela [**variável de membro CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




