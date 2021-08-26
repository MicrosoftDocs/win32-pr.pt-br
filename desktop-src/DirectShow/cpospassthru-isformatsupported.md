---
description: 'Método CPosPassThru. IsFormatSupported – o método IsFormatSupported determina se há suporte para um formato de hora especificado. Esse método implementa o método IMediaSeeking:: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Método CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d4ae6cee00879d9778380e76249ddc786f40be007081bb5aa8d78a4da2f4f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084086"
---
# <a name="cpospassthruisformatsupported-method"></a>Método CPosPassThru. IsFormatSupported

O `IsFormatSupported` método determina se há suporte para um formato de hora especificado. Esse método implementa o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Ponteiro para um GUID de formato de hora.

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

 

 




