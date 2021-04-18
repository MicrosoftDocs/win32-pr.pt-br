---
title: Estrutura de CD3DX12_BLEND_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura Desc do D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Estrutura de CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791485"
---
# <a name="cd3dx12_blend_desc-structure"></a>\_Estrutura desc de Blend CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ Desc do D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um CD3DX12 \_ Blend \_ desc.

</dd> <dt>

**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ desc& o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ Blend \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

</dd> <dt>

**CD3DX12 \_ Blend \_ DESC (padrão CD3DX12 \_ ) explícito**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ Blend \_ DESC, inicializada com parâmetros padrão.



| Estado                                   | Valor padrão                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ 0 \] . BlendEnable           | **FALSE**                        |
| RenderTarget \[ 0 \] . LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ 0 \] . SrcBlend              | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlend             | D3D12 \_ Blend \_ zero               |
| RenderTarget \[ 0 \] . BlendOp               | \_ \_ Adicionar op D3D12 \_ Blend            |
| RenderTarget \[ 0 \] . SrcBlendAlpha         | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlendAlpha        | D3D12 \_ Blend \_ zero               |
| RenderTarget \[ 0 \] . BlendOpAlpha          | \_ \_ Adicionar op D3D12 \_ Blend            |
| RenderTarget \[ 0 \] . LogicOp               | \_NOOP de \_ op \_ lógico D3D12           |
| RenderTarget \[ 0 \] . RenderTargetWriteMask | \_ \_ \_ Habilitar tudo para gravação de cores do D3D12 \_ |



 

</dd> <dt>

**~ CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ Blend \_ desc.

</dd> <dt>

**\_const do operador D3D12 Blend \_ desc& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 de \_ combinação \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





