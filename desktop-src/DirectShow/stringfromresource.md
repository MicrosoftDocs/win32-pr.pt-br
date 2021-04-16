---
description: A função StringFromResource carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso fornecido.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Função StringFromResource (Wxutil. h)
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
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758669"
---
# <a name="stringfromresource-function"></a>Função StringFromResource

A `StringFromResource` função carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso fornecido.

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

Ponteiro para a cadeia de caracteres correspondente a *iResourceID*.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso da cadeia de caracteres a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a mesma cadeia de caracteres de *pBuffer*. Se a função não for bem-sucedida, retorna uma cadeia de caracteres nula.

## <a name="remarks"></a>Comentários

O buffer *pBuffer* deve ter no mínimo \_ bytes de comprimento máximo de Str \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares de página de propriedades](property-page-helper-functions.md)
</dt> </dl>

 

 




