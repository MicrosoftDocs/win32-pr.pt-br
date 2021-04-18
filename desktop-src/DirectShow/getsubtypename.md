---
description: A função GetSubtypeName recupera o nome legível por humanos de um subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Função GetSubtypeName (Wxutil. h)
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
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750276"
---
# <a name="getsubtypename-function"></a>Função GetSubtypeName

A `GetSubtypeName` função recupera o nome legível por humanos de um subtipo de vídeo.

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

Ponteiro para um **GUID** de subtipo de vídeo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma cadeia de caracteres que contém o nome.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




