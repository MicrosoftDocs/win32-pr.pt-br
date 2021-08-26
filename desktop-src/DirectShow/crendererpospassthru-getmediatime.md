---
description: Método CRendererPosPassThru.GetMediaTime – o método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b8eb4bdd9426d589476265133234bdf3c2d5cfc691bfaced743cc4e75769c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084116"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Método CRendererPosPassThru.GetMediaTime

O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual. Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Não há suporte para conversão nesse formato.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Argumento de ponteiro **NULL.**<br/>                  |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CPosPassThru::GetMediaTime.**](cpospassthru-getmediatime.md) Os valores de carimbo de data/hora são convertidos no formato de hora atual chamando o [**método CPosPassThru::ConvertTimeFormat.**](cpospassthru-converttimeformat.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




