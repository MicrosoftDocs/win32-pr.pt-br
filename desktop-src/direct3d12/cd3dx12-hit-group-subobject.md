---
title: CD3DX12_HIT_GROUP_SUBOBJECT classe (D3dx12.h)
description: Uma classe auxiliar para criar um subobjeto de estado do grupo de acertos.
keywords:
- CD3DX12_HIT_GROUP_SUBOBJECT classe
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
ms.openlocfilehash: dd2b396e1305d2cf21cb2121aaa6a186c47d7677
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813095"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>CD3DX12_HIT_GROUP_SUBOBJECT classe

Uma classe auxiliar para criar um subobjeto de estado do grupo de acertos.

Para obter mais informações sobre os Auxiliares de Criação de Objeto de Estado D3DX12, [consulte CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

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

Construtor padrão. Cria uma nova instância inicializada por padrão de um **CD3DX12_HIT_GROUP_SUBOBJECT**.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_HIT_GROUP_SUBOBJECT** inicializado com o conteúdo de um [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) objeto .

`SetHitGroupExport(LPCWSTR)`

Função para definir o nome do grupo de acertos.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Função para definir um valor da [enumeração D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) especificando o tipo do grupo de acertos.

`SetAnyHitShaderImport(LPCWSTR)`

Função para, opcionalmente, definir o nome do sombreador de qualquer acerto associado ao grupo de acertos.

`SetClosestHitShaderImport(LPCWSTR)`

Função para, opcionalmente, definir o nome do sombreador de acerto mais próximo associado ao grupo de acertos.

`SetIntersectionShaderImport(LPCWSTR)`

Função para, opcionalmente, definir o nome do nome opcional do sombreador de interseção associado ao grupo de acertos.

`Type`

Recupera o tipo do subobjeto, representado pela [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) constante.

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a um [objeto D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) constante que descreve o objeto de estado.

`operator const D3D12_HIT_GROUP_DESC&`

Operador de conversão que retorna uma referência a um [objeto D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) constante que descreve o objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
