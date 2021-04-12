---
description: Cria um objeto Font. Observação em vez de usar essa função, recomendamos que você use DirectWrite e a biblioteca DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Função D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298546"
---
# <a name="d3dx10createfontindirect-function"></a>Função D3DX10CreateFontIndirect

Cria um objeto Font.

> [!Note]  
> Em vez de usar essa função, recomendamos que você use [DirectWrite](../directwrite/direct-write-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteFont** Class.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ponteiro para uma interface de [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

</dd> <dt>

*pDesc* \[ no\]
</dt> <dd>

Tipo: **const [**D3DX10 \_ Font \_ desc**](d3dx10-font-desc.md) \***

Ponteiro para uma [**estrutura \_ \_ desc de fonte D3DX10**](d3dx10-font-desc.md) , descrevendo os atributos do objeto Font a ser criado. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontIndirectW. Caso contrário, a chamada de função é resolvida como D3DXCreateFontIndirectA porque as cadeias de caracteres ANSI estão sendo usadas.

</dd> <dt>

*ppFont* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Retorna um ponteiro para uma [**interface ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
