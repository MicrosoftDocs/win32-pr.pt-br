---
description: 'Método CPosPassThru. SetRate-o método SetRate define a taxa de reprodução. Esse método implementa o método IMediaSeeking:: SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Método CPosPassThru. SetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095214"
---
# <a name="cpospassthrusetrate-method"></a>Método CPosPassThru. SetRate

O `SetRate` método define a taxa de reprodução. Esse método implementa o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dRate* 
</dt> <dd>

Taxa de reprodução. Não deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ INVALIDARG se *drate* for zero. Caso contrário, retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




