---
title: Estrutura de CD3DX12_TILE_SHAPE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de forma de bloco D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Estrutura de CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b02f699ab06ef93f3eeace3ce515b0947030e4824e2cb0fa51034c3e33f51dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987866"
---
# <a name="cd3dx12_tile_shape-structure"></a>Estrutura da forma do \_ bloco CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ forma de bloco D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Forma do bloco CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ forma de bloco CD3DX12 \_ .

</dd> <dt>

**\_forma de bloco CD3DX12 explícita \_ (forma de bloco const D3D12 \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ forma de bloco CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ forma de bloco D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

</dd> <dt>

**\_ \_ Forma de bloco CD3DX12 (UINT WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**
</dt> <dd>

Cria uma nova instância de uma \_ forma de bloco CD3DX12 \_ , inicializando os seguintes parâmetros:

WidthInTexels UINT

HeightInTexels UINT

DepthInTexels UINT

</dd> <dt>

**const D3D12 da \_ \_& forma de bloco const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Forma do bloco D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





