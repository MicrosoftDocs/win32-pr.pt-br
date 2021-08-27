---
description: Método CSourceSeeking.IsFormatSupported – o método IsFormatSupported determina se há suporte para um formato de hora especificado. Esse método implementa o método IMediaSeeking::IsFormatSupported.
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Método CSourceSeeking.IsFormatSupported (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92349ab37fb677b561f342e99882c27208287310b544880e397f4f5df6cb0c38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083916"
---
# <a name="csourceseekingisformatsupported-method"></a>Método CSourceSeeking.IsFormatSupported

O método determina se há suporte `IsFormatSupported` para um formato de hora especificado. Esse método implementa o [**método IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pformat* 
</dt> <dd>

Ponteiro para um GUID de formato de hora. Consulte [**GUIDs de formato de hora.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Não há suporte para o formato .<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Há suporte para o formato .<br/>     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | Argumento de ponteiro **NULL.**<br/>   |



 

## <a name="remarks"></a>Comentários

O único formato de tempo com suporte da classe base é TIME FORMAT MEDIA TIME (unidades de \_ \_ \_ 100 nanossegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




