---
description: A função WideStringFromResource carrega uma cadeia de caracteres largos de um arquivo de recurso com o identificador de recurso fornecido.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Função WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798f915536c491d32ccab7e7dbdc9b506d8b5df22b4459818472307e62356b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071810"
---
# <a name="widestringfromresource-function"></a>Função WideStringFromResource

A `WideStringFromResource` função carrega uma cadeia de caracteres largos de um arquivo de recurso com o identificador de recurso fornecido.

## <a name="syntax"></a>Sintaxe


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
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

## <a name="return-value"></a>Valor retornado

Retorna a mesma cadeia de caracteres de *pBuffer*. Se a função não for bem-sucedida, retorna uma cadeia de caracteres nula.

## <a name="remarks"></a>Comentários

As páginas de propriedades são geralmente chamadas por meio de suas interfaces COM, que usam cadeias de caracteres largos, independentemente de como o binário é compilado. Essa função permite converter uma cadeia de caracteres de recurso em uma cadeia de caracteres largos. A função converte o recurso em uma cadeia de caracteres largos (se ainda não for um) depois de carregá-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares de página de propriedades](property-page-helper-functions.md)
</dt> </dl>

 

 




