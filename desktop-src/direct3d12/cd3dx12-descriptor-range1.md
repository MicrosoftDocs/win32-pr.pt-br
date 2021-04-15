---
title: Estrutura de CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura RANGE1 do descritor D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Estrutura de CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747458"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>\_Estrutura RANGE1 do descritor CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ RANGE1 do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ descritor CD3DX12 \_ RANGE1.

</dd> <dt>

**\_descritor CD3DX12 explícito \_ RANGE1 (const D3D12 \_ Descriptor \_ RANGE1 &o)**
</dt> <dd>

Cria uma nova instância de um \_ descritor CD3DX12 \_ RANGE1, inicializada com o conteúdo de outra estrutura [**\_ \_ RANGE1 do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

</dd> <dt>

**CD3DX12 \_ Descriptor \_ RANGE1 (D3D12 \_ descritor de intervalo de tipo RangeType \_ \_ , uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ flags = D3D12 \_ \_ sinalizador de intervalo de descritor \_ \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ acrescentar)**
</dt> <dd>

Cria uma nova instância de um \_ descritor CD3DX12 \_ RANGE1, inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> <dt>

**Init embutido (D3D12 \_ de intervalo de descritor de \_ \_ tipo RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ flags = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição \_ \_ \_ acrescentar)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> <dt>

**Inicialização embutida estática ( \_ descritor de D3D12 \_ RANGE1 &intervalo, D3D12 descritor de intervalo de \_ \_ \_ tipo RangeType, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descritor \_ sinalizadores de intervalo sinalizadores \_ = D3D12 \_ descritor de \_ intervalo \_ Flag \_ nenhum, uint offsetInDescriptorsFromTableStart = D3D12 \_ descritor de intervalo de descrição de \_ \_ deslocamento \_**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Intervalo \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) de &de RANGE1 do descritor

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ intervalo de descritores**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) flags = \_ sinalizador de intervalo de descritor D3D12 \_ \_ \_ None

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ descritor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





