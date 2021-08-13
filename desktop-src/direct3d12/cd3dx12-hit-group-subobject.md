---
title: Classe CD3DX12_HIT_GROUP_SUBOBJECT (D3dx12. h)
description: Uma classe auxiliar para criar um subobjeto de estado de grupo de acesso.
keywords:
- Classe CD3DX12_HIT_GROUP_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 68b95f15c41fd46bfaeb58943720d3b657a3208d9a0276e9ab65fe7bd6087c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037354"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>Classe CD3DX12_HIT_GROUP_SUBOBJECT

Uma classe auxiliar para criar um subobjeto de estado de grupo de acesso.

Para obter mais informações sobre os auxiliares de criação de objeto de estado D3DX12, consulte [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>Membros

`CD3DX12_HIT_GROUP_SUBOBJECT`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_HIT_GROUP_SUBOBJECT**.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_HIT_GROUP_SUBOBJECT** inicializado com o conteúdo de um objeto [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetHitGroupExport(LPCWSTR)`

Função para definir o nome do grupo de acesso.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Função para definir um valor da enumeração [D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) especificando o tipo do grupo de acesso.

`SetAnyHitShaderImport(LPCWSTR)`

Função para definir opcionalmente o nome do sombreador de qualquer clique associado ao grupo de pressionamentos de clique.

`SetClosestHitShaderImport(LPCWSTR)`

Para definir opcionalmente o nome do sombreador de clique mais próximo associado ao grupo de acesso.

`SetIntersectionShaderImport(LPCWSTR)`

Função para definir opcionalmente o nome do sombreador de interseção associado ao grupo de acesso.

`Type`

Recupera o tipo do subobjeto, representado pela constante [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a uma constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que descreve o objeto de estado.

`operator const D3D12_HIT_GROUP_DESC&`

Operador de conversão que retorna uma referência a uma constante [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) objeto que descreve o objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
