---
description: Especifica se a cor especificada é uma cor RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Função FRGBIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 135a53a6c531d14f03aa2bc944e076f51ec28c167bced94cc0675fe2ae7642ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404660"
---
# <a name="frgbimecolorstyle-function"></a>Função FRGBIMEColorStyle

Especifica se a cor especificada é uma cor RGB.

## <a name="syntax"></a>Sintaxe


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcolorstyle* \[ Em\]
</dt> <dd>

Uma **estrutura IMECOLORSTY** retornada de [**uma função PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle.**](pcolorstyletextfromimestyle.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE** quando a cor é uma cor RGB.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

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

 

 
