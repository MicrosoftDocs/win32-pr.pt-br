---
title: CD3DX12_BLEND_DESC (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ BLEND \_ DESC.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC estrutura
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
ms.openlocfilehash: 40acdedbe428d808a576b68645a3e662dc71389b4d6dd0c19424278f28deb93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989946"
---
# <a name="cd3dx12_blend_desc-structure"></a>Estrutura CD3DX12 \_ BLEND \_ DESC

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ BLEND \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

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

**CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ BLEND \_ DESC.

</dd> <dt>

**EXPLICIT CD3DX12 \_ BLEND \_ DESC(const D3D12 \_ BLEND \_ DESC& o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 BLEND DESC, inicializado com o conteúdo de outra \_ \_ estrutura [**D3D12 \_ BLEND \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

</dd> <dt>

**CD3DX12 \_ BLEND \_ DESC explícito (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ BLEND \_ DESC, inicializado com parâmetros padrão.



| Estado                                   | Valor padrão                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ \] 0. BlendEnable           | **FALSE**                        |
| RenderTarget \[ \] 0. LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ \] 0. SrcBlend              | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlend             | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOp               | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. SrcBlendAlpha         | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlendAlpha        | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOpAlpha          | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. LogicOp               | NOOP DE OPERAÇÃO LÓGICA D3D12 \_ \_ \_           |
| RenderTarget \[ \] 0. RenderTargetWriteMask | D3D12 \_ COLOR \_ WRITE \_ ENABLE \_ ALL |



 

</dd> <dt>

**~CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ BLEND \_ DESC.

</dd> <dt>

**operator const D3D12 \_ BLEND \_ DESC&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





