---
title: Estrutura de CD3DX12_BOX (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de caixa D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Estrutura de CD3DX12_BOX
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
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807158"
---
# <a name="cd3dx12_box-structure"></a>Estrutura da caixa de CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ caixa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

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

**\_Caixa de CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ caixa CD3DX12.

</dd> <dt>

**caixa CD3DX12 explícita \_ (const D3D12 \_ Box& o)**
</dt> <dd>

Cria uma nova instância de uma \_ caixa CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ caixa de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

</dd> <dt>

**caixa CD3DX12 explícita \_ (esquerda longa, longa direita)**
</dt> <dd>

Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:

LONGA para a esquerda

LONGO direito

</dd> <dt>

**caixa CD3DX12 explícita \_ (esquerda longa, longa superior, longa direita, longa parte inferior)**
</dt> <dd>

Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:

LONGA para a esquerda

Início longo

LONGO direito

Parte inferior longa

</dd> <dt>

**caixa CD3DX12 explícita \_ (longa esquerda, longa superior, frente longo, longa direita, longa parte inferior, longa volta)**
</dt> <dd>

Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:

LONGA para a esquerda

Início longo

Frente longo

LONGO direito

Parte inferior longa

LONGO retorno

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Destrói uma instância de uma caixa CD3DX12 \_ .

</dd> <dt>

**\_const da& caixa D3D12 de operador const () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Caixa de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





