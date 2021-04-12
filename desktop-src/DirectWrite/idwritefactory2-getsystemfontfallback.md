---
title: Método IDWriteFactory2 GetSystemFontFallback
description: Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Gravação direta do método GetSystemFontFallback
- Método GetSystemFontFallback Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366461"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Método IDWriteFactory2:: GetSystemFontFallback

Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fontFallback* \[ fora\]
</dt> <dd>

Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Contém um endereço de um ponteiro para o objeto de fallback de fonte recém-criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 