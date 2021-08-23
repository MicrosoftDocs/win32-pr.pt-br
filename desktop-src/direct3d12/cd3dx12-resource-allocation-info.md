---
title: CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO.
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO estrutura
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
ms.openlocfilehash: 63915f2fa05950ad96bc621b9887b1c4fe23149e22ba408767d111f7b74d6927
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729216"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>Estrutura CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ RESOURCE ALLOCATION \_ \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

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

**CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ o)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 RESOURCE ALLOCATION INFO, inicializada com o conteúdo de outra \_ \_ estrutura \_ [**D3D12 \_ RESOURCE ALLOCATION \_ \_ INFO.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

</dd> <dt>

**CD3DX12 \_ RESOURCE ALLOCATION INFO \_ \_ (tamanho UINT64, alinhamento UINT64)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO, inicializando os seguintes parâmetros:

Tamanho UINT64

Alinhamento UINT64

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ ALLOCATION INFO \_&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ INFORMAÇÕES DE \_ ALOCAÇÃO DE \_ RECURSOS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





