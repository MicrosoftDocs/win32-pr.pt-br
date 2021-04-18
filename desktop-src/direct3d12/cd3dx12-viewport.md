---
title: Estrutura de CD3DX12_VIEWPORT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura viewport D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Estrutura de CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791610"
---
# <a name="cd3dx12_viewport-structure"></a>\_Estrutura do visor CD3DX12

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ viewport D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Visor CD3DX12 ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um visor CD3DX12 \_ .

</dd> <dt>

**visor CD3DX12 explícito \_ (const D3D12 \_ viewport& o)**
</dt> <dd>

Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:

const D3D12 \_ VIEWPORT& o

</dd> <dt>

**visor CD3DX12 explícito \_ (float topLeftX, float topLeftY, largura de float, altura flutuante, float minDepth = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:

TopLeftX flutuante

TopLeftY flutuante

Largura flutuante

Altura do FLOAT

FLOAT minDepth = \_ profundidade mínima de D3D12 \_

FLOAT maxDepth = \_ profundidade máxima de D3D12 \_

</dd> <dt>

**visor CD3DX12 explícito \_ (ID3D12Resource \* de origem, uint mipSlice = 0, float topLeftX = 0,0 f, float topLeftY = 0,0 f, float MINDEPTH = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:

ID3D12Resource de \* origem

UINT mipSlice = 0

FLOAT topLeftX = 0,0 f

FLOAT topLeftY = 0,0 f

FLOAT minDepth = \_ profundidade mínima de D3D12 \_

FLOAT maxDepth = \_ profundidade máxima de D3D12 \_

</dd> <dt>

**~ CD3DX12 \_ viewport ()**
</dt> <dd>

Destrói uma instância de um visor D3DX12 \_ .

</dd> <dt>

**\_const do operador D3D12 VIEWPORT& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Visor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





