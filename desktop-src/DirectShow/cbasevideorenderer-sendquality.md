---
description: O método SendQuality envia uma mensagem de qualidade para indicar o que o fornecedor deve fazer sobre a qualidade.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Método CBaseVideoRenderer. SendQuality (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074760"
---
# <a name="cbasevideorenderersendquality-method"></a>Método CBaseVideoRenderer. SendQuality

O `SendQuality` método envia uma mensagem de qualidade para indicar o que o fornecedor deve fazer sobre a qualidade.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*trLate* 
</dt> <dd>

Período de tempo pelo qual o quadro está atrasado.

</dd> <dt>

*trRealStream* 
</dt> <dd>

Tempo de Currentstream.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro envia uma mensagem de controle de qualidade upstream para controlar o gerenciamento de qualidade. A natureza da mensagem de qualidade (ou seja, se deseja reduzir ou aumentar o número de amostras) é determinada na implementação de gerenciamento de qualidade nessa classe derivada (consulte [**CBaseVideoRenderer:: ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




