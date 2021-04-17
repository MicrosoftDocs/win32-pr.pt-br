---
title: Estrutura de CD3DX12_HEAP_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de heap D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Estrutura de CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762334"
---
# <a name="cd3dx12_heap_desc-structure"></a>\_Estrutura desc de heap CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ de heap DESC ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um CD3DX12 de \_ heap \_ desc.

</dd> <dt>

**heap CD3DX12 \_ explícito \_ DESC (const D3D12 \_ heap \_ desc &o)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (tamanho UInt64, propriedades de heap de D3D12 \_ \_ , alinhamento de UINT64 = 0, D3D12 sinalizadores de \_ heap sinalizadores \_ = D3D12 \_ heap \_ Flag \_ nenhum)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

Tamanho de UINT64

[**D3D12 \_ Propriedades de \_ Propriedades do heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

opt Alinhamento de UINT64 = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (tamanho UInt64, \_ \_ tipo de heap D3D12, alinhamento de UInt64 = 0, sinalizadores de \_ sinalizadores de heap D3D12 \_ = sinalizador de heap de D3D12 \_ \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

Tamanho de UINT64

[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

opt Alinhamento de UINT64 = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (tamanho de UInt64, \_ propriedade de página de CPU D3D12 \_ \_ cpuPageProperty, D3D12 de \_ \_ pool de memória memoryPoolPreference, alinhamento de UINT64 = 0, sinalizadores de \_ sinalizadores de heap D3D12 \_ = sinalizador de heap D3D12 \_ \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

Tamanho de UINT64

[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

opt Alinhamento de UINT64 = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ heap propriedades propriedades \_ , sinalizadores de heap de D3D12 \_ \_ flags = D3D12 \_ sinalizador de heap \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Propriedades de \_ Propriedades do heap**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ \_ tipo de heap, \_ sinalizadores de heap D3D12 \_ flags = \_ sinalizador de heap D3D12 \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ informações de alocação de recursos \_& resAllocInfo, D3D12 \_ CPU \_ Page \_ Property CPUPAGEPROPERTY, D3D12 \_ \_ pool de memória memoryPoolPreference, D3D12 \_ heap \_ flags flags = D3D12 \_ \_ sinalizador heap \_ None)**
</dt> <dd>

Cria uma nova instância de um \_ heap CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = sinalizador de heap D3D12 \_ \_ \_ nenhum

</dd> <dt>

**const do operador const D3D12 \_ \_ de HEAP desc& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de \_ estrutura desc de heap CD3DX12 \_ .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 de \_ heap \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





