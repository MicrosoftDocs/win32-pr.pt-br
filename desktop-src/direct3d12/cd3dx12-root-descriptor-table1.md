---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura table1 do descritor raiz D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761596"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>\_ \_ Estrutura table1 do descritor raiz CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ table1 do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ do descritor raiz \_ Table1 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ \_ descritor raiz CD3DX12 \_ table1.

</dd> <dt>

**\_ \_ descritor de raiz CD3DX12 explícito \_ Table1 (const D3D12 \_ raiz \_ Descriptor \_ Table1 &o)**
</dt> <dd>

Cria uma nova instância de um \_ \_ descritor raiz CD3DX12 \_ Table1, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ table1 do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

</dd> <dt>

**CD3DX12 \_ \_ Descriptor raiz \_ Table1 (UINT NUMDESCRIPTORRANGES, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Cria uma nova instância de um \_ \_ descritor raiz CD3DX12 \_ Table1, inicializando os seguintes parâmetros:

NumDescriptorRanges UINT

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**Init embutido (UINT numDescriptorRanges, D3D12 const \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumDescriptorRanges UINT

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**Inicialização embutida estática (D3D12 o \_ \_ descritor raiz \_ Table1 &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Descritor raiz \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable

NumDescriptorRanges UINT

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ do \_ descritor raiz \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





