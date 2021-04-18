---
title: Estrutura de CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de coordenada de recursos lado-a-D3D12 \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Estrutura de CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761522"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>\_Estrutura de \_ coordenada de recursos lado-a-CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ coordenada de recursos lado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) -a-D3D12.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Coordenada de recurso do lado do CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ coordenada de recurso de lado CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ \_ coordenada de recurso CD3DX12 de lado explícito (constante D3D12 de recurso em ladrilho de const \_ \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ coordenada de recurso do lado do CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ coordenada de recurso de lado D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

</dd> <dt>

**\_ \_ \_ Coordenada de recurso do lado do CD3DX12 (UINT x, UINT y, uintstate z, uint preresource)**
</dt> <dd>

Cria uma nova instância de uma \_ coordenada de recurso do lado do CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

X UINT

Y UINT

Z UINT

Subrecurso UINT

</dd> <dt>

**constante \_ \_ de recurso const D3D12 \_ de coordenadas de recursos de lado& () const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ \_ Coordenada de recurso de lado D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





