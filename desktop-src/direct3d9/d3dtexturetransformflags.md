---
description: Define valores de transformação da coordenada de textura.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumeração D3DTEXTURETRANSFORMFLAGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 514b8066b19ea5a3f558d9edee7cd57bae69dbb443e9b662a0209c9b57b58f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096601"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Enumeração D3DTEXTURETRANSFORMFLAGS

Define valores de transformação da coordenada de textura.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ DISABLE**
</dt> <dd>

As coordenadas de textura são passadas diretamente para o rasterizador.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

O rasterizador deve esperar coordenadas de textura 1D. Esse valor é usado pelo processamento de vértice de função fixa; ele deve ser definido como 0 ao usar um sombreador de vértice programável.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

O rasterizador deve esperar coordenadas de textura 2D. Esse valor é usado pelo processamento de vértice de função fixa; ele deve ser definido como 0 ao usar um sombreador de vértice programável.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

O rasterizador deve esperar coordenadas de textura 3D. Esse valor é usado pelo processamento de vértice de função fixa; ele deve ser definido como 0 ao usar um sombreador de vértice programável.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

O rasterizador deve esperar coordenadas de textura 4D. Esse valor é usado pelo processamento de vértice de função fixa; ele deve ser definido como 0 ao usar um sombreador de vértice programável.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ PROJETADO**
</dt> <dd>

Esse sinalizador é honorado pelo pipeline de pixel de função fixa, bem como pelo pipeline de pixel programável nas versões ps \_ 1 \_ 1 a ps \_ 1 \_ 3. Quando a projeção de textura é habilitada para um estágio de textura, todos os quatro valores de ponto flutuante devem ser gravados no registro de textura correspondente. Cada coordenada de textura é dividida pelo último elemento antes de ser passada para o rasterizador. Por exemplo, se esse sinalizador for especificado com o sinalizador D3DTTFF COUNT3, a primeira e a segunda coordenadas de textura serão divididas pela terceira coordenada antes de serem passadas para o \_ rasterizador.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

As coordenadas de textura podem ser transformadas usando uma matriz 4 x 4 antes que os resultados sejam passados para o rasterizador. As transformação de coordenadas de textura são definidas chamando [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api)e passando o estado do estágio de textura TEXTURETRANSFORMFLAGS do D3DTS E um dos valores \_ **de D3DTEXTURETRANSFORMFLAGS**. Para obter mais informações sobre transformações de textura, consulte [Transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
