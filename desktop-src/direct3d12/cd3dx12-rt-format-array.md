---
title: Estrutura de CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de matriz de formato D3D12 RT \_ \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Estrutura de CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762493"
---
# <a name="cd3dx12_rt_format_array-structure"></a>\_Estrutura de \_ matriz de formato CD3DX12 RT \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Matriz de formato CD3DX12 RT \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ matriz de \_ formato CD3DX12 RT \_ .

</dd> <dt>

**\_ \_ matriz de formato CD3DX12 RT explícita \_ (matriz de formato const D3D12 \_ RT \_ \_& o)**
</dt> <dd>

Cria uma nova instância de uma \_ matriz de formato CD3DX12 RT \_ \_ , inicializada com valores copiados de uma estrutura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**\_ \_ matriz de formato CD3DX12 RT explícita \_ (const dxgi \_ Format \* pFormats, uint NumFormats)**
</dt> <dd>

Cria uma nova instância de uma \_ matriz de formato CD3DX12 RT \_ \_ , inicializada com os valores passados na lista de parâmetros. O conteúdo da matriz especificada pelo parâmetro *pFormats* é copiado para a matriz de membros **RTFormats**. Pressupõe-se que a matriz especificada por *pFormats* tenha o mesmo tamanho que **RTFormats**.

</dd> <dt>

**\_ \_ matriz de formato const D3D12 RT do operador \_& () const**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Como a \_ \_ matriz de formato D3D12 RT \_ é o tipo subjacente de \_ DESC1 estêncil de profundidade CD3DX12 \_ \_ , o objeto é simplesmente retornado como uma referência de matriz de formato const D3D12 \_ RT \_ \_ para si mesmo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Matriz de \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





