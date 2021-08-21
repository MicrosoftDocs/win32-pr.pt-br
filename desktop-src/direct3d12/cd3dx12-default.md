---
title: CD3DX12_DEFAULT (D3dx12.h)
description: Passa D3D12 \_ DEFAULT para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT estrutura
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
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531283"
---
# <a name="cd3dx12_default-structure"></a>Estrutura CD3DX12 \_ DEFAULT

Passa D3D12 \_ DEFAULT para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares.

## <a name="remarks"></a>Comentários

Este struct é declarado da seguinte forma:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Passa D3D12 \_ DEFAULT para um construtor para cada struct auxiliar. Por exemplo, o construtor a seguir é declarado em d3dx12.h:

CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(CD3DX12 \_ DEFAULT) { ptr = 0; }

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





