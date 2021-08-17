---
title: Método GetSystemFontFallback de IDWriteFactory2
description: Cria um objeto de fallback de fonte da lista de fallback de fonte do sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Gravação direta do método GetSystemFontFallback
- Método GetSystemFontFallback Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface Direct Write , GetSystemFontFallback method
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4513c8ee7fb4e7a3796ec442d4d36bb663a0c8803bb6276a584edcfda306d588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329436"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Método IDWriteFactory2::GetSystemFontFallback

Cria um objeto de fallback de fonte da lista de fallback de fonte do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fontFallback* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contém um endereço de um ponteiro para o objeto de fallback de fonte recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 