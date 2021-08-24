---
description: Especifica se um estilo que não é de cor tem o estilo itálico.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Função FItalicIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c8160edf46b97544ef27558bf15a8a58e447e78a0e0709432aea840f4567bc0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076110"
---
# <a name="fitalicimestyle-function"></a>Função FItalicIMEStyle

Especifica se um estilo que não é de cor tem o estilo itálico.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pimestyle* \[ Em\]
</dt> <dd>

Uma **estrutura IMESTYLE** retornada da [**função PIMEStyleFromAttr.**](pimestylefromattr.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**TRUE** se o estilo tiver o estilo itálico.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
