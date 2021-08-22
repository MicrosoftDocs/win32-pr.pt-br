---
title: CD3DX12_DESCRIPTOR_RANGE1 (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ DESCRIPTOR \_ RANGE1.
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 estrutura
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
ms.openlocfilehash: 404cb41a019dac404bbe351f78f1d1e65277dd9ad2aecf2cc2d94d06fe242f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989876"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>Estrutura CD3DX12 \_ DESCRIPTOR \_ RANGE1

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ DESCRIPTOR \_ RANGE1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

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

**CD3DX12 \_ DESCRIPTOR \_ RANGE1()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ DESCRIPTOR \_ RANGE1.

</dd> <dt>

**EXPLICIT CD3DX12 \_ DESCRIPTOR \_ RANGE1(const D3D12 \_ DESCRIPTOR \_ RANGE1 &o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 DESCRIPTOR RANGE1, inicializado com o conteúdo de outra \_ \_ estrutura [**D3D12 \_ DESCRIPTOR \_ RANGE1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 SINALIZADORES RANGE \_ DESCRIPTOR = \_ \_ D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ DESCRIPTOR \_ RANGE1, inicializando os seguintes parâmetros:

[**D3D12 \_ RANGE \_ TYPE \_ rangeType DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

NumDescriptors UINT

UINT baseShaderRegister

RegisterSpace UINT = 0

[**D3D12 \_ SINALIZADORES \_ DE SINALIZADORES \_ DE INTERVALO DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) DESCRITOR = D3D12 SINALIZADOR DE INTERVALO DO \_ \_ \_ DESCRITOR \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ \_ \_ DESCRIPTOR RANGE TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 SINALIZADORES RANGE \_ DESCRIPTOR RANGE = \_ \_ D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RANGE \_ TYPE \_ rangeType DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

NumDescriptors UINT

UINT baseShaderRegister

RegisterSpace UINT = 0

[**D3D12 \_ SINALIZADORES \_ DE SINALIZADORES \_ DE INTERVALO DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) DESCRITOR = D3D12 SINALIZADOR DE INTERVALO DO \_ \_ \_ DESCRITOR \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE1 &intervalo, D3D12 \_ \_ \_ DESCRIPTOR RANGE TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 SINALIZADORES RANGE \_ RANGE = \_ \_ D3D12 \_ DESCRIPTOR \_ RANGE FLAG \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE OFFSET \_ \_ APPEND)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Intervalo de &DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

[**D3D12 \_ RANGE \_ TYPE \_ rangeType DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

NumDescriptors UINT

UINT baseShaderRegister

RegisterSpace UINT = 0

[**D3D12 \_ SINALIZADORES \_ DE SINALIZADORES \_ DE INTERVALO DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) DESCRITOR = D3D12 SINALIZADOR DE INTERVALO DO \_ \_ \_ DESCRITOR \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





