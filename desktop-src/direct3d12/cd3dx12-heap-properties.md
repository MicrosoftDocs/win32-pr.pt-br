---
title: Estrutura de CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de propriedades de heap D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Estrutura de CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811461"
---
# <a name="cd3dx12_heap_properties-structure"></a>Estrutura de propriedades do \_ heap CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ Propriedades de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Propriedades de heap CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma CD3DX12 de \_ heap de \_ Propriedades.

</dd> <dt>

**\_Propriedades de heap CD3DX12 explícitas \_ (const D3D12 \_ heap \_ Propriedades &o)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializada com o conteúdo de outra estrutura de [**\_ \_ Propriedades de heap D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

</dd> <dt>

**\_ \_ Propriedades de heap CD3DX12 ( \_ propriedade de página de CPU D3D12 \_ \_ cpuPageProperty, D3D12 \_ \_ pool de memória MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Propriedade da página da CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference do \_ pool de memória**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

opt UINT creationNodeMask = 1

opt UINT nodeMask = 1

</dd> <dt>

**\_Propriedades de heap CD3DX12 explícitas \_ ( \_ \_ tipo de tipo de heap D3D12, uint CREATIONNODEMASK = 1, uint nodeMask = 1)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ heap \_ Propriedades, inicializando os seguintes parâmetros:

[**D3D12 \_ Tipo de \_ tipo de heap**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

opt UINT creationNodeMask = 1

opt UINT nodeMask = 1

</dd> <dt>

**\_const do operador D3D12 \_ de propriedades de heap& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> <dt>

**operador embutido = = (const D3D12 \_ heap \_ Propriedades& l, const D3D12 \_ heap \_ Propriedades& r)**
</dt> <dd>

Testes de igualdade entre as instâncias de \_ Propriedades de heap D3D12 especificadas \_ , com base na igualdade de todos os campos de membro.

</dd> <dt>

**operador embutido! = (const D3D12 \_ heap \_ Propriedades& l, const D3D12 \_ heap \_ Propriedades& r)**
</dt> <dd>

Testa a desigualdade entre as instâncias de propriedades de heap D3D12 especificadas \_ \_ . Implementado ao tirar o inverso do **operador = =** valor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Propriedades de heap D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





