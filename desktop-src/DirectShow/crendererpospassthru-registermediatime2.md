---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual. Esse método usa os parâmetros *StartTime* e *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parâmetros StartTime e EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187827"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parâmetros StartTime e EndTime

O método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) armazena em cache os carimbos de data/hora do exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* 
</dt> <dd>

Hora de início da amostra, em unidades de 100 a nanossegundos.

</dd> <dt>

*EndTime* 
</dt> <dd>

Hora de término da amostra, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método armazena os valores de carimbo de data/hora fornecidos em *StartTime* e *EndTime*. O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.

O filtro deve chamar esse método para cada amostra que receber. O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Ctlutil. h (incluir fluxos. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |



 

 




