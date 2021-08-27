---
title: Estrutura de CD3DX12_VIEW_INSTANCING_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Estrutura de CD3DX12_VIEW_INSTANCING_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813255"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>Estrutura de CD3DX12_VIEW_INSTANCING_DESC

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Sintaxe

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_VIEW_INSTANCING_DESC`

Construtor padrão. Cria uma nova instância, não inicializada, de um **CD3DX12_VIEW_INSTANCING_DESC**.

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_VIEW_INSTANCING_DESC** inicializado com o conteúdo de uma estrutura de [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Construtor que cria uma nova instância de um **CD3DX12_VIEW_INSTANCING_DESC** inicializado com esses valores.

|Membro de dados|valor|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Flags|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Construtor que cria uma nova instância de um **CD3DX12_VIEW_INSTANCING_DESC** inicializado com os parâmetros passados a ele.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
