---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de descritor raiz D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771322"
---
# <a name="cd3dx12_root_descriptor-structure"></a>\_Estrutura do \_ descritor raiz CD3DX12

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Descritor raiz CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ descritor de raiz CD3DX12 \_ .

</dd> <dt>

**\_ \_ descritor de raiz CD3DX12 explícito ( \_ descritor de raiz const D3D12 \_ &o)**
</dt> <dd>

Cria uma nova instância de um \_ \_ descritor raiz CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

</dd> <dt>

**\_ \_ Descritor raiz CD3DX12 (UINT SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Cria uma nova instância de um \_ \_ descritor raiz CD3DX12, inicializando os seguintes parâmetros:

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> <dt>

**Init embutido (UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> <dt>

**Inicialização embutida estática ( \_ \_ descritor raiz D3D12 &tabela, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Descritor raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &tabela

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ \_ Descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





