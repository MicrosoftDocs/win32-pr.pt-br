---
title: Estrutura de CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de informações de alocação de recursos D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Estrutura de CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807980"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>\_Estrutura de \_ informações de alocação de recursos CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ informações de \_ alocação \_ de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Informações de alocação de recursos do CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ informação de alocação de recurso CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ informações de alocação de recursos CD3DX12 explícitas \_ (const D3D12 \_ informações de alocação de recursos \_ \_& o)**
</dt> <dd>

Cria uma nova instância de uma \_ informação de alocação de recursos CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de informações de [**alocação de recursos do D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

</dd> <dt>

**\_ \_ \_ Informações de alocação de recursos CD3DX12 (tamanho de UInt64, alinhamento de UInt64)**
</dt> <dd>

Cria uma nova instância de uma \_ informação de alocação de recursos CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

Tamanho de UINT64

Alinhamento de UINT64

</dd> <dt>

**const D3D12 \_ \_ \_& informações de alocação de recurso**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Informações de \_ alocação de recursos do D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





