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
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759305"
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

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




