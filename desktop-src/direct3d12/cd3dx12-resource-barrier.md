---
title: Estrutura de CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de barreira de recursos D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Estrutura de CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788612"
---
# <a name="cd3dx12_resource_barrier-structure"></a>Estrutura de barreira de \_ recursos CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ barreira de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Barreira de recurso CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ barreira de recurso CD3DX12 \_ .

</dd> <dt>

**\_ \_ barreira de recurso de CD3DX12 explícita ( \_ barreira de recurso D3D12 const \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ barreira de recurso CD3DX12 \_ , inicializada com o conteúdo de outra [**\_ \_ barreira de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).

</dd> <dt>

**Transição embutida estática (ID3D12Resource de \* origem, D3D12 de \_ recursos do \_ stateBefore, D3D12 de \_ Estados de recursos \_ stateAfter, subresource uint = D3D12 \_ barreira de recursos \_ \_ todos os \_ subrecursos, D3D12 sinalizadores de \_ barreira de recurso \_ \_ sinalizadores = D3D12 \_ sinalizador de barreira de recurso \_ \_ \_ nenhum)**
</dt> <dd>

Transições entre os Estados de recursos, usando os seguintes parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* origem

[**D3D12 \_ StateBefore de \_ Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

[**D3D12 \_ StateAfter de \_ Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

opt Subrecurso UINT = [ **D3D12 de \_ recurso para \_ \_ todos os \_ subrecursos**](constants.md)

opt [**D3D12 \_ Sinalizadores \_ \_ sinalizadores de barreira de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = sinalizador de barreira de recurso D3D12 \_ \_ \_ \_ nenhum

</dd> <dt>

**Alias embutido estático (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Cria aliases para o recurso antes e depois da transição de barreira. Parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**UAV embutido estático ( \* PreSource ID3D12Resource)**
</dt> <dd>

Cria um UAV (modo de exibição de acesso não ordenado) para o recurso. Parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* origem

</dd> <dt>

**\_const do operador D3D12 \_ de barreira de recurso constante& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Barreira de recurso D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





