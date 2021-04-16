---
description: A função DbgOutString envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Função DbgOutString (Wxdebug. h)
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
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747578"
---
# <a name="dbgoutstring-function"></a>Função DbgOutString

A função **DbgOutString** envia uma cadeia de caracteres para o local de saída de depuração. Ignorado em compilações de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psz* 
</dt> <dd>

Cadeia de caracteres para saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Em compilações de depuração, essa função sempre gera a cadeia de caracteres, independentemente dos níveis de saída de depuração atuais. Para ter um controle mais preciso sobre a saída, use a macro [**DbgLog**](dbglog.md) .

## <a name="examples"></a>Exemplos


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




