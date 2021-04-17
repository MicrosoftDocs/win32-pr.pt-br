---
description: Especifica se um estilo sem cor tem um estilo sublinhado.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: Função FUlIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747881"
---
# <a name="fulimestyle-function"></a>Função FUlIMEStyle

Especifica se um estilo sem cor tem um estilo sublinhado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pimestyle* \[ no\]
</dt> <dd>

Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

TRUE se o estilo tiver um estilo sublinhado.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
