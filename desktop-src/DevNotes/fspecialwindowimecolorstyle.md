---
description: Especifica se a cor especificada é uma cor de janela especial.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: Função FSpecialWindowIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c42a8f4cf61b2b61d228dc243d06e902d825040570f4baa6502f2feba0322ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691336"
---
# <a name="fspecialwindowimecolorstyle-function"></a>Função FSpecialWindowIMEColorStyle

Especifica se a cor especificada é uma cor de janela especial.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcolorstyle* \[ no\]
</dt> <dd>

Uma estrutura **IMECOLORSTY** retornada de uma função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** quando a cor é uma cor de janela especial (uma cor especial).

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
