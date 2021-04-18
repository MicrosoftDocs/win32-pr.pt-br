---
title: Estrutura de CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de subrecurso do D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764208"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>\_Estrutura de SUBrecurso do CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**SubCD3DX12 \_ de subrecurso \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ subrecurso do CD3DX12 \_ .

</dd> <dt>

**subdivisão \_ de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ subrecurso do \_ &o)**
</dt> <dd>

Cria uma nova instância de um subCD3DX12 de \_ subrecurso \_ , inicializado com o conteúdo de outra estrutura de [**\_ subrecurso \_ do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

</dd> <dt>

**SubCD3DX12 \_ de subrecurso \_ (UINT WIDTHINTILES, UInt16 HEIGHTINTILES, UInt16 DEPTHINTILES, uint startTileIndexInOverallResource)**
</dt> <dd>

Cria uma nova instância de um subCD3DX12 de \_ subrecurso \_ , inicializando os seguintes parâmetros:

WidthInTiles UINT

UINT16 heightInTiles

UINT16 depthInTiles

StartTileIndexInOverallResource UINT

</dd> <dt>

**\_ \_ const de D3D12 de sub& recurso do operador const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SubD3D12 de \_ SUBrecurso \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





