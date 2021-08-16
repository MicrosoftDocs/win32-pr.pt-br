---
title: CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT classe (D3dx12.h)
description: Uma classe auxiliar para criar um subobjeto que define as propriedades gerais de um objeto de estado.
keywords:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT classe
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 294dda04f9550e437f91f6f5595206a4113a975ee182ac900b6c4804b3100fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346553"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT classe

Uma classe auxiliar para criar um subobjeto que define as propriedades gerais de um objeto de estado.

Para obter mais informações sobre os Auxiliares de Criação de Objeto de Estado D3DX12, [consulte CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

Construtor padrão. Cria uma nova instância inicializada por padrão de um **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**.

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** inicializado com o conteúdo de um [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

Função para especificar os requisitos para o objeto de estado por meio [de um D3D12_STATE_OBJECT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) objeto .

`Type`

Recupera o tipo do subobjeto, representado pela [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a um [objeto D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) constante que descreve o objeto de estado.

`operator const D3D12_STATE_OBJECT_CONFIG&`

Operador de conversão que retorna uma referência a um [objeto D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) constante que descreve o objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
