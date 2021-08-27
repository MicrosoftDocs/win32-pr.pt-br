---
title: Classe CD3DX12_DXIL_LIBRARY_SUBOBJECT (D3dx12. h)
description: Uma classe auxiliar para criar um subobjeto de estado de biblioteca DXIL.
keywords:
- Classe CD3DX12_DXIL_LIBRARY_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_DXIL_LIBRARY_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 33ec22dd722469ce131bc58d5aca83f0aed4edf0
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812551"
---
# <a name="cd3dx12_dxil_library_subobject-class"></a>Classe CD3DX12_DXIL_LIBRARY_SUBOBJECT

Uma classe auxiliar para criar um subobjeto de estado de biblioteca DXIL.

Para obter mais informações sobre os auxiliares de criação de objeto de estado D3DX12, consulte [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_DXIL_LIBRARY_SUBOBJECT
{
    CD3DX12_DXIL_LIBRARY_SUBOBJECT() noexcept;
    CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    void SetDXILLibrary(const D3D12_SHADER_BYTECODE* pCode) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_DXIL_LIBRARY_DESC& () const noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_DXIL_LIBRARY_SUBOBJECT`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_DXIL_LIBRARY_SUBOBJECT**.

`CD3DX12_DXIL_LIBRARY_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_DXIL_LIBRARY_SUBOBJECT** inicializado com o conteúdo de um objeto [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetDXILLibrary(const D3D12_SHADER_BYTECODE*)`

Função para definir a biblioteca DXIL na forma do ponteiro para um [D3D12_SHADER_BYTECODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) passado como o parâmetro.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Define um símbolo exportado do subobjeto. Usa um [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) como um parâmetro opcional.

`DefineExports(LPCWSTR(&)[N]);`

Define uma matriz de *N* símbolos exportados do subobjeto. Parâmetro de modelo *N* especifica o número de elementos na matriz.

`DefineExports(const LPCWSTR*, UINT)`

Define uma matriz de símbolos exportados do subobjeto.

`Type`

Recupera o tipo do subobjeto, representado pela constante [D3D12_STATE_SUBOBJECT_TYPE_DXIL_LIBRARY](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) .

`operator const D3D12_STATE_SUBOBJECT&`

Operador de conversão que retorna uma referência a uma constante [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) objeto que descreve o objeto de estado.

`operator const D3D12_DXIL_LIBRARY_DESC&`

Operador de conversão que retorna uma referência a uma constante [**D3D12_DXIL_LIBRARY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_library_desc) objeto que descreve o objeto de estado.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
