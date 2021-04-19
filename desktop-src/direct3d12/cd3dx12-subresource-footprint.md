---
title: Estrutura de CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de superfície de subrecurso do D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_FOOTPRINT
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
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812024"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>\_Estrutura de superfície do SUBrecurso do CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ superfície de subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

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

**CD3DX12 da \_ \_ superfície do subrecurso ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ superfície de SUBRECURSO CD3DX12 \_ .

</dd> <dt>

**\_superfície de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ superfície do subrecurso \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ superfície de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

</dd> <dt>

**\_Superfície de SUBRECURSO CD3DX12 \_ ( \_ formato de formato dxgi, largura UINT, altura UINT, profundidade uint, semidensidade uint)**
</dt> <dd>

Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializando os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Largura de UINT

Altura UINT

Profundidade de UINT

Semidensidade UINT

</dd> <dt>

**\_superfície de SUBRECURSO CD3DX12 explícito \_ (const D3D12 \_ recurso \_ desc& RESDESC, semidensidade uint)**
</dt> <dd>

Cria uma nova instância de uma \_ superfície de SUBRECURSO CD3DX12 \_ , inicializando os seguintes parâmetros:

[**D3D12 \_ RECURSO \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

Semidensidade UINT

</dd> <dt>

**constante de D3D12 \_ de subrecurso \_ de constante de operador de& () const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Superfície do SUBrecurso do D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

