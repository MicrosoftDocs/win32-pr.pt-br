---
title: Estrutura de D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indica o estado do dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Estrutura D3DX11_STATE_BLOCK_MASK Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298721"
---
# <a name="d3dx11_state_block_mask-structure"></a>\_Estrutura de \_ máscara de bloco de estado D3DX11 \_

Indica o estado do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Membros

<dl> <dt>

**VS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador de vértice deve ser salvo.

</dd> <dt>

**VSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostras de Vertex-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**VSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos de sombreador de vértice. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante de sombreador de vértice. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.

</dd> <dt>

**VSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de vértice. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**HS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador envoltória deve ser salvo.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostragens envoltória-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos envoltória-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante envoltória-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.

</dd> <dt>

**HSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces envoltória-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**AD**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador do domínio deve ser salvo.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostras de sombreador de domínio. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos de sombreador de domínio. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante de sombreador de domínio. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer.

</dd> <dt>

**DSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de domínio. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**GS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador de geometria deve ser salvo.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostragens Geometry-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos Geometry-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante Geometry-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer.

</dd> <dt>

**GSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces Geometry-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**PROFISSIONAIS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador de pixel deve ser salvo.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostras de sombreador de pixel. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos de sombreador de pixel. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante de sombreador de pixel. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.

</dd> <dt>

**PSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de pixel. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se as exibições de acesso não ordenadas do sombreador de pixel devem ser salvas.

</dd> <dt>

**CS**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do sombreador de computação deve ser salvo.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de amostras de sombreador de computação. A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de recursos de sombreador de computação. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de constante Compute-Shader. A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.

</dd> <dt>

**CSInterfaces**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de interfaces de sombreador de computação. A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se as exibições de acesso não ordenadas do sombreador de computação devem ser salvas.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Matriz de buffers de vértice. A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do buffer de índice deve ser salvo.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado de layout de entrada deve ser salvo.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado da topologia primitiva deve ser salvo.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se os Estados de destino de renderização devem ser salvos.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado de estêncil de profundidade deve ser salvo.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado de mesclagem deve ser salvo.

</dd> <dt>

**RSViewports**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se os Estados de visores devem ser salvos.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se os Estados dos retângulos da mola devem ser salvos.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado do rasterizador deve ser salvo.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se os Estados de buffers de saída de streaming devem ser salvos.

</dd> <dt>

**Predicação**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor booliano que indica se o estado predicação deve ser salvo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma máscara de bloco de estado indica que o dispositivo informa que uma passagem ou uma técnica altera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

