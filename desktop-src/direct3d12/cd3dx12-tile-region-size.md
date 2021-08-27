---
title: CD3DX12_TILE_REGION_SIZE (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ TILE \_ REGION \_ SIZE.
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- CD3DX12_TILE_REGION_SIZE estrutura
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
ms.openlocfilehash: 9cc1b96ae4d7d33101068a1ba08f0314b99950146e91a352ab49fea714376471
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119606"
---
# <a name="cd3dx12_tile_region_size-structure"></a>Estrutura CD3DX12 \_ TILE \_ REGION \_ SIZE

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ TILE \_ REGION \_ SIZE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

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

**CD3DX12 \_ TAMANHO DA REGIÃO DO \_ \_ TILE()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ TILE \_ REGION \_ SIZE.

</dd> <dt>

**EXPLICIT CD3DX12 \_ TILE \_ REGION \_ SIZE(const D3D12 \_ TILE \_ REGION SIZE \_ &o)**
</dt> <dd>

Cria uma nova instância de um TAMANHO DA REGIÃO DE UM TILE CD3DX12, inicializado com o conteúdo de outra estrutura \_ \_ \_ [**D3D12 TAMANHO DA REGIÃO \_ \_ \_ DO TILE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)

</dd> <dt>

**CD3DX12 TAMANHO DA REGIÃO DO \_ TILE \_ \_ (uint numTiles, bool useBox, largura UINT, altura UINT16, profundidade UINT16)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ TILE \_ REGION \_ SIZE, inicializando os seguintes parâmetros:

NumTiles UINT

BOOL useBox

Largura UINT

Altura UINT16

Profundidade UINT16

</dd> <dt>

**operator const D3D12 \_ TILE \_ REGION SIZE \_&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TAMANHO DA REGIÃO DO TILE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





