---
title: CD3DX12_CLEAR_VALUE (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ CLEAR \_ VALUE.
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE estrutura
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
ms.openlocfilehash: 785ab3c8312949bfc692fcd7c8d1dace28734ce08e5763387a744eb28f2000f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988486"
---
# <a name="cd3dx12_clear_value-structure"></a>Estrutura CD3DX12 \_ CLEAR \_ VALUE

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ CLEAR \_ VALUE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

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

**CD3DX12 \_ CLEAR \_ VALUE()**
</dt> <dd>

Cria uma nova instância não reinicializada de um CD3DX12 \_ CLEAR \_ VALUE.

</dd> <dt>

**EXPLICIT CD3DX12 \_ CLEAR \_ VALUE(const D3D12 \_ CLEAR VALUE &\_ o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 CLEAR VALUE, inicializado com o conteúdo de outra \_ \_ estrutura [**D3D12 \_ CLEAR \_ VALUE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(formato DXGI, \_ const FLOAT color \[ 4 \] )**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ CLEAR \_ VALUE, inicializando os seguintes parâmetros:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Cor FLOAT \[ 4 \]

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE (formato DXGI, \_ profundidade FLOAT, estêncil UINT8)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ CLEAR \_ VALUE, inicializando os seguintes parâmetros:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Profundidade float

Estêncil UINT8

</dd> <dt>

**operator const D3D12 \_ CLEAR \_ VALUE&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ CLEAR \_ VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

