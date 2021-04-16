---
title: Estrutura de CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de valor claro D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Estrutura de CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747664"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ limpar \_ estrutura de valor

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ valor claro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ limpar \_ valor ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ valor de limpeza CD3DX12 \_ .

</dd> <dt>

**\_valor de limpeza CD3DX12 explícito \_ (const D3D12 \_ limpar \_ valor &o)**
</dt> <dd>

Cria uma nova instância de um valor de limpeza de CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ valor de limpeza D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

</dd> <dt>

**CD3DX12 \_ \_ valor de limpeza ( \_ formato de formato dxgi, cor de float de const \[ 4 \] )**
</dt> <dd>

Cria uma nova instância de um \_ valor de limpeza CD3DX12 \_ , inicializando os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Cor de FLUTUAção \[ 4 \]

</dd> <dt>

**CD3DX12 \_ \_ valor de limpeza ( \_ formato de formato dxgi, profundidade flutuante, estêncil UINT8)**
</dt> <dd>

Cria uma nova instância de um \_ valor de limpeza CD3DX12 \_ , inicializando os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Profundidade de FLUTUAção

Estêncil UINT8

</dd> <dt>

**const D3D12 do operador const \_ \_ de valor limpo& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ limpar \_ valor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

