---
title: CD3DX12_BOX (D3dx12.h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura D3D12 \_ BOX.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX estrutura
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: f2aa358d8b2d772d45c6387221dd9e660a9630fbf90535ada7dcceefc3257879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851406"
---
# <a name="cd3dx12_box-structure"></a>Estrutura CD3DX12 \_ BOX

Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**estrutura D3D12 \_ BOX.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ BOX()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ BOX.

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(const D3D12 \_ BOX& o)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 BOX, inicializado com o conteúdo de outra \_ [**estrutura D3D12 \_ BOX.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Right)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ BOX, inicializando os seguintes parâmetros:

LONG Left

LONG Right

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ BOX, inicializando os seguintes parâmetros:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**EXPLICIT CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ BOX, inicializando os seguintes parâmetros:

LONG Left

LONG Top

Frente LONGA

LONG Right

LONG Bottom

LONG Back

</dd> <dt>

**~CD3DX12 \_ BOX()**
</dt> <dd>

Destrói uma instância de um CD3DX12 \_ BOX.

</dd> <dt>

**operator const D3D12 \_ BOX&() const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





