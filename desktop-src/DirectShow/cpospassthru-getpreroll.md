---
description: 'O método GetPreroll recupera a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b34cd565d246f4401061834b21c005306633e72a6f24cc8367a222b5f3736c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954035"
---
# <a name="cpospassthrugetpreroll-method"></a>Método CPosPassThru. GetPreroll

O `GetPreroll` método recupera a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de preversão, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




