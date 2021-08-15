---
title: Classe CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT (D3dx12. h)
description: Uma classe auxiliar para criar um subobjeto de estado de associação de subobjeto para exportação.
keywords:
- Classe CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 07fc8ba911e1f16c6cec96752b658b1578d998bd0d9a469016fb8506f3dbc85d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132248"
---
# <a name="cd3dx12_subobject_to_exports_association_subobject-class"></a>Classe CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT

Uma classe auxiliar para criar um subobjeto de estado de associação de subobjeto para exportação.

Para obter mais informações sobre os auxiliares de criação de objeto de estado D3DX12, consulte [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT
{
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT() noexcept;
    CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT& SubobjectToAssociate) noexcept;
    void AddExport(LPCWSTR Export);
    template<size_t N> void AddExports(LPCWSTR(&Exports)[N]);
    void AddExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION& () const noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**.

`CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT** inicializado com o conteúdo de um objeto [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetSubobjectToAssociate(const D3D12_STATE_SUBOBJECT&)`

Função para definir o subobjeto a ser associado na forma de um [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) passado como o parâmetro.

`AddExport(LPCWSTR)`

Adiciona uma exportação para associar.

`AddExports(LPCWSTR(&)[N]);`

Adiciona uma matriz de exportações para associar. Parâmetro de modelo *N* especifica o número de elementos na matriz.

`AddExports(const LPCWSTR*, UINT)`

Define uma matriz de *N* exportações a serem associadas.

`Type`

Recupera o tipo do subobjeto, representado pela constante [D3D12_STATE_SUBOBJECT_TYPE_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a uma constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que descreve o objeto de estado.

`operator const D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION&`

Operador de conversão que retorna uma referência a uma constante [D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION](/windows/win32/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association) objeto que descreve o objeto de estado.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
