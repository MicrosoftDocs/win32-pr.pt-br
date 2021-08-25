---
description: O método IsUsingTimeFormat determina se um formato de hora especificado é o formato atualmente em uso.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking.IsUsingTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b930746102bc43e3549b4565a7591f4ac5fee8cc6503d9fb6aadcbe1659a52f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054236"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Método CSourceSeeking.IsUsingTimeFormat

O `IsUsingTimeFormat` método determina se um formato de hora especificado é o formato atualmente em uso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsUsingTimeFormat(
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



| Código de retorno                                                                               | Descrição                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | O formato especificado não é o formato atual.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | O formato especificado é o formato atual.<br/>     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | Argumento de ponteiro **NULL.**<br/>                      |



 

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

 

 




