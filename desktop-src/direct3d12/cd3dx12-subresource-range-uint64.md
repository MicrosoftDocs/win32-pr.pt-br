---
title: Estrutura de CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura UINT64 de intervalo de subrecursos do D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Estrutura de CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808257"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>\_ \_ Estrutura UINT64 do intervalo de subrecursos do CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ UINT64 de \_ intervalo \_ de subrecursos do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ do intervalo de subrecurso \_ UINT64 ()**
</dt> <dd>

Cria uma nova instância não inicializada de um CD3DX12 do \_ intervalo de subrecurso \_ \_ UINT64.

</dd> <dt>

**\_intervalo de SUBRECURSO CD3DX12 explícito \_ \_ UINT64 (const D3D12 \_ intervalo de subrecurso \_ \_ UInt64 &o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 do \_ intervalo de subrecurso \_ \_ UINT64, inicializada com valores copiados de uma estrutura UInt64 do [**\_ \_ intervalo \_ de subrecurso do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

</dd> <dt>

**CD3DX12 \_ do intervalo de subrecurso \_ \_ UInt64 (subrecurso uint, D3D12 do \_ intervalo de& const \_ UINT64)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.

</dd> <dt>

**CD3DX12 \_ do intervalo de subrecurso \_ \_ UINT64 (subrecurso uint, UINT64 Begin, UInt64 end)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.

</dd> <dt>

**D3D12 const \_ \_ de subconjunto de subrecurso \_ UINT64& () const**
</dt> <dd>

Conversão implícita em uma \_ estrutura UINT64 do intervalo de SUBrecursos do D3D12 \_ \_ . Como \_ o intervalo de SUBrecursos do D3D12 \_ \_ UInt64 é o tipo subjacente do \_ intervalo de subrecursos do CD3DX12 \_ \_ UInt64, o objeto é simplesmente retornado como um estêncil const D3D12 \_ Depth \_ \_ DESC1 referência a si mesmo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 do \_ intervalo de subrecurso \_ \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





