---
title: CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT estrutura
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32c3da3e133a5509543ffaa4fbf80b4c565730f13d3b9e92753658c96efcfcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069726"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>Estrutura DE ESPAÇO DE \_ SUBRESOURCE CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT.

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ SUBRESOURCE \_ FOOTPRINT &o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 SUBRESOURCE FOOTPRINT, inicializado com o conteúdo de outra estrutura \_ \_ [**D3D12 \_ SUBRESOURCE \_ FOOTPRINT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(formato DXGI \_ FORMAT, largura UINT, altura UINT, profundidade UINT, rowPitch UINT)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT, inicializando os seguintes parâmetros:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Largura UINT

Altura da UINT

Profundidade UINT

RowPitch UINT

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ RESOURCE \_ DESC& resDesc, UINT rowPitch)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT, inicializando os seguintes parâmetros:

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

RowPitch UINT

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ FOOTPRINT&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ESPAÇO DE \_ SUBRESOURCE D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

