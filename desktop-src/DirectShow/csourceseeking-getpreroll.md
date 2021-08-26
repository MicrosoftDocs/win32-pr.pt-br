---
description: O método GetPreroll recupera o tempo de pré-pagamento. Esse método implementa o método IMediaSeeking::GetPreroll.
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Método CSourceSeeking.GetPreroll (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2d20c4487f0969a5abaf689f7c5c712e6fbb7fd83ceb7484694a3eec8599698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083956"
---
# <a name="csourceseekinggetpreroll-method"></a>Método CSourceSeeking.GetPreroll

O `GetPreroll` método recupera o tempo de pré-roll. Esse método implementa o [**método IMediaSeeking::GetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPreroll* 
</dt> <dd>

Ponteiro para uma variável que recebe o tempo de pré-roll. O valor é definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | **Valor do** ponteiro NULL<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




