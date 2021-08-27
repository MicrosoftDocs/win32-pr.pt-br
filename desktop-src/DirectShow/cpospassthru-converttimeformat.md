---
description: 'Método CPosPassThru. ConvertTimeFormat-o método ConvertTimeFormat converte de um formato de tempo para outro. Esse método implementa o método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2382d36899bf7e3ac85e217502a878497274604ced4b77cf7acbc1465586c487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954115"
---
# <a name="cpospassthruconverttimeformat-method"></a>Método CPosPassThru. ConvertTimeFormat

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

Ponteiro para o GUID de formato de hora do formato de destino. Se for **NULL**, o formato atual será usado.

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

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUIDs de formato de hora**](time-format-guids.md)
</dt> </dl>

 

 




