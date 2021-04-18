---
title: Estrutura de CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de estêncil de profundidade de D3D12 \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Estrutura de CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750520"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>\_ \_ Estrutura desc de estêncil de profundidade de CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**desc de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Estêncil de profundidade \_ de CD3DX12 DESC ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ estêncil de profundidade D3DX12 \_ \_ desc.

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC (const D3D12 \_ Depth \_ estêncil \_ desc& o)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de D3DX12 \_ \_ \_ DESC, inicializada com o conteúdo de outra estrutura [**desc de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de um \_ estêncil de profundidade D3DX12 \_ \_ DESC, inicializada com parâmetros padrão.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC (bool depthEnable, D3D12 \_ profundidade \_ Write \_ Mask depthWriteMask, D3D12 \_ Comparison \_ Func DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ estêncil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op frontStencilDepthFailOp, D3D12 \_ estêncil op \_ frontStencilPassOp, D3D12 \_ Comparison Func frontStencilFunc, D3D12 \_ \_ estêncil op backStencilFailOp \_ , D3D12 \_ stencil \_ \_ \_ \_ \_ op backStencilDepthFailOp, D3D12 estêncil op backStencilPassOp, D3D12 Comparison Func backStencilFunc)**
</dt> <dd>

Cria uma nova instância de um \_ estêncil de profundidade D3DX12 \_ \_ DESC, inicializando os seguintes parâmetros:

DepthEnable BOOL

[**D3D12 \_ \_ \_ Máscara de gravação de profundidade**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

StencilEnable BOOL

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_ FrontStencilFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ FrontStencilDepthFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ FrontStencilPassOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ BackStencilFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ BackStencilDepthFailOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ BackStencilPassOp \_ op de estêncil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ COMPARAÇÃO de \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~ \_ \_ Estêncil de profundidade \_ de CD3DX12 DESC ()**
</dt> <dd>

Destrói uma instância de um estêncil de \_ profundidade \_ CD3DX12 \_ desc.

</dd> <dt>

**\_const D3D12 de profundidade \_ de estêncil const \_& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





