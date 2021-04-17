---
title: Estrutura de CD3DX12_DEFAULT (D3dx12. h)
description: Passa \_ o padrão D3D12 para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- Estrutura de CD3DX12_DEFAULT
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748071"
---
# <a name="cd3dx12_default-structure"></a>\_Estrutura padrão CD3DX12

Passa \_ o padrão D3D12 para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.

## <a name="remarks"></a>Comentários

Essa estrutura é declarada da seguinte maneira:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Passa \_ o padrão D3D12 para um construtor para cada struct auxiliar. Por exemplo, o Construtor a seguir é declarado em d3dx12. h:

\_ \_ Identificador do descritor de CPU CD3DX12 \_ ( \_ padrão CD3DX12) {PTR = 0;}

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





