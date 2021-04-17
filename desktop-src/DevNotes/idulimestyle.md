---
description: Identifica se o estilo sem cor especificado tem sublinhado.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Função IdUlIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752574"
---
# <a name="idulimestyle-function"></a>Função IdUlIMEStyle

Identifica se o estilo sem cor especificado tem sublinhado.

## <a name="syntax"></a>Sintaxe


```C++
UINT __cdecl IdUlIMEStyle(
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

Essa função pode retornar um dos valores a seguir.

<dl> <dt>

**IMESTY \_ UL \_ mín** (2002)
</dt> <dt>

**IMESTY \_ UL \_ None** (2002)
</dt> <dt>

**IMESTY \_ UL \_ único** (2003)
</dt> <dt>

**IMESTY \_ UL \_ pontilhado** (2005)
</dt> <dt>

**IMESTY \_ UL \_ espessa** (2006)
</dt> <dt>

**IMESTY \_ UL \_ inferior** (2011)
</dt> <dt>

**IMESTY \_ UL \_ THICKLOWER** (2012)
</dt> <dt>

**IMESTY \_ UL \_ THICKDITHLOWER** (2013)
</dt> <dt>

**IMESTY \_ UL \_ DITHLOWER** (2014)
</dt> <dt>

**IMESTY \_ UL \_ Max** (2014)
</dt> </dl>

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

 

 
