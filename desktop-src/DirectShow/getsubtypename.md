---
description: A função GetSubtypeName recupera o nome acessível por humanos de um subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Função GetSubtypeName (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c676f3e08f55bd010e761853b777e0eb4b28933536ab7af09bd94e457032b583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564844"
---
# <a name="getsubtypename-function"></a>Função GetSubtypeName

A `GetSubtypeName` função recupera o nome acessível por humanos de um subtipo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSubtype* 
</dt> <dd>

Ponteiro para um GUID de subtipo **de vídeo.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma cadeia de caracteres que contém o nome.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




