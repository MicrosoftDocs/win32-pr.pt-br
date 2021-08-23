---
title: CD3DX12_RECT (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ RECT.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT estrutura
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
ms.openlocfilehash: bff9df3a4c7df2f30e9614b16d5f8b89ea1b6f0279a1566b206cabef7260fb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729336"
---
# <a name="cd3dx12_rect-structure"></a>Estrutura DE RECT CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ RECT.**](d3d12-rect.md)

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

**CD3DX12 \_ RECT()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ RECT.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(const D3D12 \_ RECT& o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 RECT, inicializado com o conteúdo de outra \_ [**estrutura D3D12 \_ RECT.**](d3d12-rect.md)

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ RECT, inicializando os seguintes parâmetros:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**~CD3DX12 \_ RECT()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ RECT.

</dd> <dt>

**operator const D3D12 \_ RECT&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ RECT**](d3d12-rect.md)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





