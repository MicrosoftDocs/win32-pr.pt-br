---
description: 'Método CSourceSeeking. GetDuration – o método GetDuration recupera a duração do fluxo. Esse método implementa o método IMediaSeeking:: getDuration.'
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
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098764"
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

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Valor de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

A duração é especificada pela variável de membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




