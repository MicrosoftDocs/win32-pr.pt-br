---
description: 'O método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking:: getDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Método CSourceSeeking. getDuration (Ctlutil. h)
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
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747377"
---
# <a name="csourceseekinggetduration-method"></a>Método CSourceSeeking. GetDuration

O `GetDuration` método recupera a duração do fluxo. Esse método implementa o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

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

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Sucesso<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Valor de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

A duração é especificada pela variável de membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




