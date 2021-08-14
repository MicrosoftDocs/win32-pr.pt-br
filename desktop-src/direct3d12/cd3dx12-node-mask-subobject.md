---
title: Classe CD3DX12_NODE_MASK_SUBOBJECT (D3dx12. h)
description: Uma classe auxiliar para criar um subobjeto de estado que identifica os nós de GPU aos quais o objeto de estado se aplica.
keywords:
- Classe CD3DX12_NODE_MASK_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_NODE_MASK_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: c71a2aa97e376a03b3f77f38a3101c26930e788403f1cef9b26e2c77d4598be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752226"
---
# <a name="cd3dx12_node_mask_subobject-class"></a>Classe CD3DX12_NODE_MASK_SUBOBJECT

Uma classe auxiliar para criar um subobjeto de estado que identifica os nós de GPU aos quais o objeto de estado se aplica.

Para obter mais informações sobre os auxiliares de criação de objeto de estado D3DX12, consulte [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_NODE_MASK_SUBOBJECT
{
    CD3DX12_NODE_MASK_SUBOBJECT() noexcept;
    CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetNodeMask(UINT NodeMask) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_NODE_MASK& () const noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_NODE_MASK_SUBOBJECT`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_NODE_MASK_SUBOBJECT**.

`CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_NODE_MASK_SUBOBJECT** inicializado com o conteúdo de um objeto [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetNodeMask(UINT)`

Função para definir a máscara de nó.

`Type`

Recupera o tipo do subobjeto, representado pela constante [D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a uma constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que descreve o objeto de estado.

`operator const D3D12_NODE_MASK&`

Operador de conversão que retorna uma referência a uma constante [D3D12_NODE_MASK](/windows/win32/api/d3d12/ns-d3d12-d3d12_node_mask) objeto que descreve o objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
