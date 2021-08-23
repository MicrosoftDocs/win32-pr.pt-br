---
description: A função StringFromResource carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso determinado.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Função StringFromResource (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329646"
---
# <a name="stringfromresource-function"></a>Função StringFromResource

A `StringFromResource` função carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso determinado.

## <a name="syntax"></a>Sintaxe


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBuffer* 
</dt> <dd>

Ponteiro para a cadeia de caracteres correspondente *a iResourceID.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso da cadeia de caracteres a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a mesma cadeia de caracteres *que pBuffer.* Se a função não for bem-sucedida, retornará uma cadeia de caracteres nula.

## <a name="remarks"></a>Comentários

O *buffer pBuffer* deve ter pelo menos bytes STR \_ MAX \_ LENGTH.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares da página de propriedades](property-page-helper-functions.md)
</dt> </dl>

 

 




