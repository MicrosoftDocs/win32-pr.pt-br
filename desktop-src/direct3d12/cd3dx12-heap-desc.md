---
title: CD3DX12_HEAP_DESC (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ HEAP \_ DESC.
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC estrutura
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
ms.openlocfilehash: 347e44a8516b48dcd779d3ac19fbc9b5bbf5d37ad565f36a0b9b10a083d395c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858366"
---
# <a name="cd3dx12_heap_desc-structure"></a>Estrutura CD3DX12 \_ HEAP \_ DESC

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ HEAP \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

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

**CD3DX12 \_ HEAP \_ DESC()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ HEAP \_ DESC.

</dd> <dt>

**EXPLICIT CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ HEAP \_ DESC &o)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, inicializada com o conteúdo de outra \_ \_ estrutura [**D3D12 \_ HEAP \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC (tamanho UINT64, propriedades DE PROPRIEDADES DE HEAP D3D12, alinhamento \_ \_ UINT64 = 0, sinalizadores DE SINALIZADORES DE HEAP D3D12 \_ = \_ D3D12 \_ HEAP FLAG \_ \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

Tamanho UINT64

[**D3D12 \_ Propriedades \_ DE PROPRIEDADES DO HEAP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) Alinhamento UINT64 = 0

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC (tamanho UINT64, tipo DE TIPO DE HEAP D3D12, alinhamento \_ \_ UINT64 = 0, sinalizadores DE SINALIZADORES DE HEAP D3D12 \_ = \_ D3D12 \_ HEAP FLAG \_ \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

Tamanho UINT64

[**D3D12 \_ Tipo DE \_ TIPO HEAP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) Alinhamento UINT64 = 0

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC (tamanho UINT64, PROPRIEDADE DA PÁGINA da CPU D3D12 \_ \_ \_ cpuPageProperty, D3D12 \_ MEMORY POOL \_ memoryPoolPreference, alinhamento UINT64 = 0, sinalizadores D3D12 SINALIZADORES DE \_ HEAP = \_ D3D12 \_ SINALIZADOR DE HEAP \_ \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

Tamanho UINT64

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) Alinhamento UINT64 = 0

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ PROPERTIES properties, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Propriedades \_ DE PROPRIEDADES DO HEAP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ TYPE type, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Tipo DE \_ TIPO HEAP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Cria uma nova instância de uma DESC de HEAP CD3DX12, \_ \_ inicializando os seguintes parâmetros:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) [**D3D12 \_ Sinalizadores \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP FLAG \_ \_ NONE

</dd> <dt>

**operator const D3D12 \_ HEAP \_ DESC&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura DESC HEAP CD3DX12. \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





