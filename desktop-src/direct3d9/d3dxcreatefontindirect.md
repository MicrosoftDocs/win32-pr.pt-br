---
description: Cria um objeto Font indiretamente para um dispositivo e uma fonte.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Função D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298741"
---
# <a name="d3dxcreatefontindirect-function"></a>Função D3DXCreateFontIndirect

Cria um objeto Font indiretamente para um dispositivo e uma fonte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao objeto Font.

</dd> <dt>

*pDesc* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXFONT \_ desc**](d3dxfont-desc.md) \***

Ponteiro para uma [**estrutura \_ desc de D3DXFONT**](d3dxfont-desc.md) , que descreve os atributos do objeto Font a ser criado. Se as configurações do compilador exigirem Unicode, o tipo de dados D3DXFONT \_ desc será resolvido para D3DXFONT \_ DESCW; caso contrário, o tipo de dados será resolvido para D3DXFONT \_ desca. Consulte Observações.

</dd> <dt>

*ppFont* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Retorna um ponteiro para uma interface [**ID3DXFont**](id3dxfont.md) , representando o objeto Font criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXCreateFontIndirectW. Caso contrário, a chamada de função é resolvida como D3DXCreateFontIndirectA porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
