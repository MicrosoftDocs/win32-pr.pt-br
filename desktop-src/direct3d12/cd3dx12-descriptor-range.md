---
title: Estrutura de CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de intervalo do descritor D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Estrutura de CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 641afe973c89d66257a8fc7b46defe2e77d8a8667094448ef58ab4beb2839b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989936"
---
# <a name="cd3dx12_descriptor_range-structure"></a>\_Estrutura do intervalo do descritor CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Intervalo do descritor de CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ intervalo de descritor D3DX12 \_ .

</dd> <dt>

**\_intervalo de descritor de CD3DX12 explícito \_ ( \_ intervalo de descritores const D3D12 \_ &o)**
</dt> <dd>

Cria uma nova instância de um \_ intervalo de descritor D3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

</dd> <dt>

**\_ \_ Intervalo de descritores de CD3DX12 (D3D12 de intervalo de \_ descritor de \_ \_ tipo RangeType, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de \_ deslocamento de intervalo de descritor \_ \_ \_ append)**
</dt> <dd>

Cria uma nova instância de um \_ intervalo de descritor D3DX12 \_ , inicializando os seguintes parâmetros:

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> <dt>

**Init embutido (D3D12 \_ de intervalo do descritor de \_ \_ tipo RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de \_ deslocamento de intervalo de descritor de \_ \_ \_ anexo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> <dt>

**Inicialização embutida estática ( \_ intervalo do descritor de D3D12 \_ &intervalo, D3D12 do \_ descritor de tipo RangeType \_ \_ , uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 do \_ intervalo de descritor de descrição \_ \_ \_ acrescentar)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Intervalo \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) de &do intervalo do descritor

[**D3D12 \_ \_ \_ Tipo de intervalo do descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) RangeType

NumDescriptors UINT

BaseShaderRegister UINT

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = \_ deslocamento de intervalo de descritor de D3D12 \_ \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Intervalo do descritor de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





