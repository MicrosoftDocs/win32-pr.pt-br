---
description: 'Método CSourceSeeking. ConvertTimeFormat-o método ConvertTimeFormat converte de um formato de tempo para outro. Esse método implementa o método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Método CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085244"
---
# <a name="csourceseekingconverttimeformat-method"></a>Método CSourceSeeking. ConvertTimeFormat

O `ConvertTimeFormat` método converte de um formato de tempo para outro. Esse método implementa o método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTarget* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora convertida.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Ponteiro para o GUID do formato de destino. Se for **NULL**, o formato atual será usado. Consulte [**GUIDs de formato de hora**](time-format-guids.md).

</dd> <dt>

*Origem* 
</dt> <dd>

Valor de tempo a ser convertido.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Ponteiro para o GUID de formato de hora do formato a ser convertido. Se for **NULL**, o formato atual será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido<br/>          |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos). Esse método retorna E \_ INVALIDARG, exceto no caso trivial, em que *PTargetFormat* e *pSourceFormat* especificam o tempo de mídia de formato de hora \_ \_ \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




