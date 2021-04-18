---
title: Estrutura de CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura UINT64 do intervalo de D3D12 \_ .
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Estrutura de CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812245"
---
# <a name="cd3dx12_range_uint64-structure"></a>Estrutura de UINT64 do \_ intervalo de CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ UINT64 do intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ do intervalo UINT64 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um CD3DX12 do \_ intervalo \_ UINT64.

</dd> <dt>

**intervalo CD3DX12 \_ explícito \_ UInt64 (const D3D12 \_ intervalo \_ UInt64 &o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 do \_ intervalo \_ UInt64, inicializada com valores copiados de uma estrutura [**\_ \_ UInt64 do intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

</dd> <dt>

**CD3DX12 \_ \_ do intervalo UINT64 (UInt64 Begin, UInt64 end)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1, inicializada com os valores passados na lista de parâmetros.

</dd> <dt>

**\_const D3D12 do intervalo \_ de variação do operador UINT64& () constante**
</dt> <dd>

Conversão implícita em uma \_ estrutura UINT64 do intervalo de D3D12 \_ . Como \_ o intervalo \_ de D3D12 UInt64 é o tipo subjacente do CD3DX12 \_ Range \_ UInt64, o objeto é simplesmente retornado como uma referência a um intervalo de D3D12 const \_ \_ para si mesmo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 do \_ intervalo \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





