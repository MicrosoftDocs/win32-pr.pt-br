---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de tabela de descritor raiz D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158f1d52be9502f3f886aebd3f0eb60a66d9b389367919bd5b941b880e2556ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098439"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>\_Estrutura da \_ tabela do descritor raiz CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ tabela de descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Tabela de descritor raiz CD3DX12 \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ tabela de \_ descritor raiz CD3DX12 \_ .

</dd> <dt>

**\_ \_ tabela de descritor de raiz CD3DX12 explícita \_ ( \_ tabela de descritores raiz const D3D12 \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ tabela de \_ descritor raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ tabela de descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

</dd> <dt>

**\_ \_ Tabela do descritor raiz CD3DX12 \_ (UINT NUMDESCRIPTORRANGES, const D3D12 do \_ descritor \_ \* \_ pDescriptorRanges)**
</dt> <dd>

Cria uma nova instância de uma \_ tabela de \_ descritor raiz CD3DX12 \_ , inicializando os seguintes parâmetros:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**Init embutido (UINT numDescriptorRanges, D3D12 de \_ descritor const \_ \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**Inicialização embutida estática ( \_ \_ tabela do descritor raiz D3D12 \_ &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 do \_ descritor do \_ intervalo \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_ \_ Tabela do descritor de raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Tabela de \_ descritor raiz D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





