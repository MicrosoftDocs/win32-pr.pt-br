---
title: Classe CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT (D3dx12. h)
description: Uma classe auxiliar para criar um estado de assinatura de raiz global suboject.
keywords:
- Classe CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 7ee327c24f5cc99fa386376be76ae0908fea19b6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812487"
---
# <a name="cd3dx12_global_root_signature_subobject-class"></a>Classe CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT

Uma classe auxiliar para criar um estado de assinatura de raiz global suboject.

Para obter mais informações sobre os auxiliares de criação de objeto de estado D3DX12, consulte [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT
{
    CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT() noexcept;
    CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetRootSignature(ID3D12RootSignature* pRootSig) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator ID3D12RootSignature* () const noexcept { return D3DX12_COM_PTR_GET(m_pRootSig); }
};
```

## <a name="members"></a>Membros

`CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**.

`CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT** inicializado com o conteúdo de um objeto [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetRootSignature(ID3D12RootSignature*)`

Função para definir a assinatura raiz na forma do ponteiro para um [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) passado como o parâmetro.

`Type`

Recupera o tipo do subobjeto, representado pela constante [D3D12_STATE_SUBOBJECT_TYPE_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a uma constante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que descreve o objeto de estado.

`operator ID3D12RootSignature*`

Operador de conversão que retorna a assinatura raiz na forma de um ponteiro para um [ID3D12RootSignature](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
