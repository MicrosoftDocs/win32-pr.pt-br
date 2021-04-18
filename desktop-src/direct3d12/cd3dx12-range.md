---
title: Estrutura de CD3DX12_RANGE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de intervalo D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Estrutura de CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785175"
---
# <a name="cd3dx12_range-structure"></a>Estrutura do intervalo de CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Intervalo de CD3DX12 ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um intervalo de CD3DX12 \_ .

</dd> <dt>

**intervalo CD3DX12 explícito \_ (const D3D12 \_ intervalo &o)**
</dt> <dd>

Cria uma nova instância de um \_ intervalo CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

</dd> <dt>

**\_Intervalo de CD3DX12 ( \_ início de tamanho t, tamanho \_ t end)**
</dt> <dd>

Cria uma nova instância de um intervalo de CD3DX12 \_ , inicializando os seguintes parâmetros:

Início de T de tamanho \_

Fim de T de tamanho \_

</dd> <dt>

**\_const de D3D12 de& intervalo constante de operador**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Intervalo de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





