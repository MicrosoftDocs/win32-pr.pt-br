---
description: Define os primitivos com suporte pelo Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Enumeração D3DPRIMITIVETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7406670b055a11f30a71677a88dc6230aecec8d7660d886b1d63f53e6e61566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527512"
---
# <a name="d3dprimitivetype-enumeration"></a>Enumeração D3DPRIMITIVETYPE

Define os primitivos com suporte pelo Direct3D.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ POINTLIST**
</dt> <dd>

Renderiza os vértices como uma coleção de pontos isolados. Esse valor não tem suporte para primitivos indexados.

</dd> <dt>

<span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**LISTA DE LINHAS D3DPT \_**
</dt> <dd>

Renderiza os vértices como uma lista de segmentos de linha reta isolados.

</dd> <dt>

<span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**
</dt> <dd>

Renderiza os vértices como uma única polilinha.

</dd> <dt>

<span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIANGLELIST**
</dt> <dd>

Renderiza os vértices especificados como uma sequência de triângulos isolados. Cada grupo de três vértices define um triângulo separado.

A ressarção de face é afetada pelo estado de renderização da ordem de winding atual.

</dd> <dt>

<span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**
</dt> <dd>

Renderiza os vértices como uma faixa de triângulo. O sinalizador de eliminação de face invertida é invertido automaticamente em triângulos com números even.

</dd> <dt>

<span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**
</dt> <dd>

Renderiza os vértices como um ventilador de triângulo.

</dd> <dt>

<span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Usar [faixas de triângulo ou](triangle-strips.md) ventiladores de triângulo [(Direct3D 9)](triangle-fans.md) geralmente é mais eficiente do que usar listas de triângulos porque menos vértices são duplicados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
