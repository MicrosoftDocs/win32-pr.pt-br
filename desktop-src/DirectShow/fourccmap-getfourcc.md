---
description: Recupera o fourcc&\# 160;DWORD do objeto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: Método FOURCCMap::GetCCCC (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 381625f5d0a585f212c8f7b076d1cd58ea5215958bf09025e1db864ce2f624b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015714"
---
# <a name="fourccmapgetfourcc-method"></a>Método FOURCCMap::GetCCCC

Recupera o **FOURCC** **DWORD do** objeto [**FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o **valor de FOURCC** **DWORD.** Observe que, se você construir um **GUID** que não foi originalmente derivado de um **FOURCC**, o valor de retorno será essencialmente aleatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Fourcc.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




