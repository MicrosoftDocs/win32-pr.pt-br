---
title: CD3DX12_DEPTH_STENCIL_DESC estrutura (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ DEPTH \_ STENCIL \_ DESC.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC estrutura
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
ms.openlocfilehash: 8fdbd7184ad6fc432beb5ba8e9585c2e9a93486acc604f875ff3a70f72e8ec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531102"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>Estrutura CD3DX12 \_ DEPTH \_ STENCIL \_ DESC

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

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

**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um D3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& o)**
</dt> <dd>

Cria uma nova instância de um D3DX12 DEPTH STENCIL DESC, inicializado com o conteúdo de outra estrutura \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Cria uma nova instância de um D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inicializado com parâmetros padrão.

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

**EXPLICIT CD3DX12 \_ \_ DEPTH \_ STENCIL DESC(BOOL depthEnable, D3D12 \_ DEPTH WRITE MASK \_ \_ depthWriteMask, D3D12 \_ COMPARISON \_ FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ STENCIL \_ OP frontStencilFailOp, D3D12 \_ STENCIL \_ OP frontStencilDepthFailOp, \_ D3D12 \_ STENCIL OP frontStencilPassOp, D3D12 \_ COMPARISON \_ FUNC frontStencilFunc, D3D12 \_ STENCIL \_ OP backStencilFailOp, D3D12 \_ STENCIL \_ OP backStencilDepthFailOp, D3D12 \_ STENCIL \_ OP backStencilPassOp, D3D12 \_ COMPARISON \_ FUNC backStencilFunc)**
</dt> <dd>

Cria uma nova instância de um D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inicializando os seguintes parâmetros:

Profundidade BOOLEnable

[**D3D12 \_ Profundidade \_ DA \_ MÁSCARA DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) GRAVAÇÃO DE PROFUNDIDADEWriteMask

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

Estêncil BooLEnable

StencilReadMask UINT8

StencilWriteMask UINT8

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_ BackStencilPassOp do \_ STENCIL OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ \_ DESC DE ESTÊNCIL \_ DE PROFUNDIDADE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





