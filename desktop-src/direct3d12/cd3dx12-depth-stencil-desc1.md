---
title: Estrutura de CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura DESC1 de estêncil de profundidade de D3D12 \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Estrutura de CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19e14002fe5245e28679a59b7ed94ab2869c008781875fa4714bd6bd33cc4705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913009"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>\_ \_ Estrutura DESC1 de estêncil de profundidade de CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**DESC1 de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12 ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um DESC1 de \_ estêncil de profundidade de CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (const D3D12 \_ Depth \_ estêncil \_ DESC1& o)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com valores copiados de uma estrutura [**\_ DESC1 de \_ estêncil \_ de profundidade D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (const D3D12 \_ Depth \_ estêncil \_ desc& o)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com valores copiados de uma estrutura [**\_ desc de \_ estêncil \_ de profundidade D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

e o membro **DepthBoundsTestEnable** adicional definido como **false**.

</dd> <dt>

**\_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12 explícito ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com o estado padrão prescrito por D3DX12:

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**\_ \_ estêncil de profundidade de CD3DX12 explícito \_ DESC1 (bool depthEnable, D3D12 \_ profundidade de gravação de \_ \_ máscara DepthWriteMask, D3D12 de \_ comparação \_ Func DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ estêncil \_ op FrontStencilFailOp, D3D12 \_ stencil \_ op frontStencilDepthFailOp, D3D12 \_ estêncil op frontStencilPassOp, D3D12 Comparison Func frontStencilFunc, D3D12 \_ estêncil op backStencilFailOp, \_ \_ \_ \_ D3D12 \_ stencil \_ op backStencilDepthFailOp, D3D12 estêncil op backStencilPassOp, D3D12 \_ Comparison Func backStencilFunc, \_ \_ \_ bool depthBoundsTestEnable)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.

</dd> <dt>

**~ CD3DX12 \_ \_ de estêncil \_ de profundidade DESC1 ()**
</dt> <dd>

Destrói uma instância de um estêncil de \_ profundidade de D3DX12 \_ \_ DESC1.

</dd> <dt>

**D3D12 \_ \_ de estêncil const \_ de profundidade de DESC1& () const**
</dt> <dd>

Conversão implícita em uma \_ estrutura DESC1 de estêncil de profundidade de D3D12 \_ \_ . Como \_ \_ o estêncil de profundidade de D3D12 \_ DESC1 é o tipo subjacente de estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, o objeto é simplesmente retornado como um estêncil de profundidade de D3D12 const \_ \_ \_ DESC1 referência a si mesmo.

</dd> <dt>

**\_ \_ const D3D12 de estêncil de profundidade de operador const \_ () constante**
</dt> <dd>

Conversão implícita em um \_ valor de \_ estrutura desc de estêncil de profundidade de D3D12 \_ . Como \_ o estêncil de profundidade D3D12 \_ \_ DESC não é o tipo subjacente de DESC1 de estêncil de profundidade de CD3DX12 \_ \_ \_ , uma nova \_ \_ instância de DESC de estêncil de profundidade D3D12 \_ é criada e retornada por valor. Observe que \_ o estêncil de profundidade D3D12 \_ \_ DESC não inclui o membro **DepthBoundsTestEnable** , portanto, esse valor é perdido na conversão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Estêncil de profundidade de D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





