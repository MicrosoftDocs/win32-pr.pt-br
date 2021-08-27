---
title: Estrutura de CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de localização de cópia de textura D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Estrutura de CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0a1ee179d2400bc04df9c3214d97d3c7a861357f33b7805e492a24f769bdba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119636"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>\_Estrutura de \_ localização de cópia de textura CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ localização de \_ cópia \_ de textura D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Local de cópia de textura CD3DX12 ()**
</dt> <dd>

Cria uma nova instância não inicializada de um \_ local de cópia de textura CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ \_ local de cópia de textura de CD3DX12 explícita (localização de cópia de textura D3D12 const \_ \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de localização de [**\_ cópia de textura \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

</dd> <dt>

**\_ \_ \_ Local de cópia de textura CD3DX12 (ID3D12Resource \* pRes)**
</dt> <dd>

Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

</dd> <dt>

**\_ \_ \_ Local de cópia de textura do CD3DX12 (ID3D12RESOURCE \* pRes, D3D12 \_ colocou a superfície do \_ subrecurso \_ const& superfície)**
</dt> <dd>

Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

[**D3D12 \_& superfície do \_ \_ espaço de SUBrecurso posicionado**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)

</dd> <dt>

**\_ \_ \_ Local de cópia de textura de CD3DX12 (ID3D12RESOURCE \* pRes, uint sub)**
</dt> <dd>

Cria uma nova instância de um \_ local de cópia de textura CD3DX12 \_ \_ , inicializando os seguintes parâmetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

Sub-UINT

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Local de \_ cópia de textura D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





