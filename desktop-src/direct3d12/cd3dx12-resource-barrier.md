---
title: CD3DX12_RESOURCE_BARRIER (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ RESOURCE \_ BARRIER.
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER estrutura
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
ms.openlocfilehash: bc3490f48e04c97c845264f514e65db390a01e115ebff7c53aca792d29f0c522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098440"
---
# <a name="cd3dx12_resource_barrier-structure"></a>Estrutura CD3DX12 \_ RESOURCE \_ BARRIER

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ RESOURCE \_ BARRIER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

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

**CD3DX12 \_ RESOURCE \_ BARRIER()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ RESOURCE \_ BARRIER.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RESOURCE \_ BARRIER(const D3D12 \_ RESOURCE BARRIER &\_ o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 RESOURCE BARRIER, inicializado com o conteúdo de outro \_ \_ [**D3D12 \_ RESOURCE \_ BARRIER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

</dd> <dt>

**static inline Transition(ID3D12Resource \* pResource, D3D12 \_ RESOURCE \_ STATES stateBefore, D3D12 \_ RESOURCE STATES \_ stateAfter, subresource UINT = D3D12 \_ RESOURCE BARRIER ALL \_ \_ \_ SUBRESOURCES, D3D12 \_ RESOURCE BARRIER \_ \_ FLAGS flagS = D3D12 \_ RESOURCE BARRIER FLAG \_ \_ \_ NONE)**
</dt> <dd>

Transições entre estados de recurso, usando os seguintes parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Presource

[**D3D12 \_ estado \_ RESOURCE STATESBefore**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

[**D3D12 \_ Estado \_ RESOURCE STATESAfter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

(opt) Sub-fonte UINT = [ **D3D12 \_ RESOURCE \_ BARRIER ALL \_ \_ SUBRESOURCES**](constants.md)

(opt) [**D3D12 \_ SINALIZADORES \_ DE \_ BARREIRA DE RECURSO**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) = D3D12 SINALIZADOR DE BARREIRA DE RECURSO \_ \_ \_ \_ NENHUM

</dd> <dt>

**static inline Aliasing(ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Cria aliases para o recurso antes e depois da transição da barreira. Parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**static inline UAV(ID3D12Resource \* pResource)**
</dt> <dd>

Cria um UAV (unordered-access-view) para o recurso. Parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Presource

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ BARRIER&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BARREIRA DE RECURSOS D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





