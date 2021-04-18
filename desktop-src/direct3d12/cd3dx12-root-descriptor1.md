---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura DESCRIPTOR1 raiz D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814406"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>\_Estrutura de \_ DESCRIPTOR1 raiz CD3DX12

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ DESCRIPTOR1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ raiz \_ DESCRIPTOR1 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ .

</dd> <dt>

**CD3DX12 \_ \_ DESCRIPTOR1 (const D3D12 \_ raiz \_ DESCRIPTOR1 &o)**
</dt> <dd>

Cria uma nova instância de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ DESCRIPTOR1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

</dd> <dt>

**CD3DX12 \_ raiz \_ DESCRIPTOR1 (UINT SHADERREGISTER, uint registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor raiz \_ flags = D3D12 \_ sinalizador do \_ descritor raiz \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ , inicializando os seguintes parâmetros:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

</dd> <dt>

**Init embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 \_ sinalizador do \_ descritor raiz \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

</dd> <dt>

**Inicialização embutida estática (D3D12 \_ raiz \_ DESCRIPTOR1 &tabela, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de descritor de raiz \_ \_ sinalizadores = \_ sinalizador de descritor raiz D3D12 \_ \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Tabela \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) de &de DESCRIPTOR1 raiz

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ raiz \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





