---
title: Estrutura de CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de tamanho de região de bloco do D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Estrutura de CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810852"
---
# <a name="cd3dx12_tile_region_size-structure"></a>\_Estrutura de \_ tamanho da região de bloco do CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**tamanho de região de bloco do D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Tamanho da \_ região do bloco CD3DX12 \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ tamanho de região de bloco CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ tamanho de região de bloco CD3DX12 explícito \_ (const D3D12 \_ tamanho da região do bloco \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de um \_ tamanho de região de bloco CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de tamanho de [**\_ região de bloco \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

</dd> <dt>

**\_Tamanho da \_ região de bloco CD3DX12 \_ (UINT NumTiles, bool useBox, largura de uint, altura de UInt16, profundidade de UInt16)**
</dt> <dd>

Cria uma nova instância de um \_ tamanho de região de bloco CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

NumTiles UINT

UseBox BOOL

Largura de UINT

Altura de UINT16

Profundidade de UINT16

</dd> <dt>

**const D3D12 \_ tamanho da \_ região \_ de bloco do operador& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Tamanho da \_ região do bloco D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





