---
title: Estrutura de CD3DX12_RECT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura RECT D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Estrutura de CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798492"
---
# <a name="cd3dx12_rect-structure"></a>\_Estrutura CD3DX12 Rect

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ Rect D3D12**](d3d12-rect.md) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um CD3DX12 \_ Rect.

</dd> <dt>

**CD3DX12 \_ Rect explícito (const D3D12 \_ Rect& o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ Rect, inicializada com o conteúdo de outra estrutura [**D3D12 \_ Rect**](d3d12-rect.md) .

</dd> <dt>

**CD3DX12 \_ Rect explícito (esquerda longa, longa superior, longa direita, longa parte inferior)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ Rect, inicializando os seguintes parâmetros:

LONGA para a esquerda

Início longo

LONGO direito

Parte inferior longa

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ Rect.

</dd> <dt>

**\_const do operador D3D12 RECT& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





