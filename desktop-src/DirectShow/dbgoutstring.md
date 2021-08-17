---
description: A função DbgOutString envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em builds de varejo.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Função DbgOutString (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821553"
---
# <a name="dbgoutstring-function"></a>Função DbgOutString

A **função DbgOutString** envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Psz* 
</dt> <dd>

Cadeia de caracteres a ser saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Em builds de depuração, essa função sempre emita a cadeia de caracteres, independentemente dos níveis de saída de depuração atuais. Para um controle mais fino sobre a saída, use a [**macro DbgLog.**](dbglog.md)

## <a name="examples"></a>Exemplos


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




