---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual. Esse método usa os *parâmetros StartTime* *e EndTime.*
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h) – parâmetros StartTime e EndTime
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
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084106"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h) – parâmetros StartTime e EndTime

O [**método RegisterMediaTime**](crendererpospassthru-registermediatime.md) armazena em cache os carimbos de data/hora do exemplo atual.

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

Hora de início de exemplo, em unidades de 100 nanossegundos.

</dd> <dt>

*EndTime* 
</dt> <dd>

Hora de término de exemplo, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método armazena os valores de carimbo de data/hora determinados *em StartTime* *e EndTime.* O [**método CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.

O filtro deve chamar esse método para cada amostra que recebe. O método é sobrecarregado para aceitar um ponteiro para o exemplo ou os próprios valores de carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Ctlutil.h (incluir Fluxos.h)                                                                                   |
| Biblioteca | Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |



 

 




