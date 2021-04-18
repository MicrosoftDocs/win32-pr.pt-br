---
title: Função D3D12DecomposeSubresource (D3dx12.h)
description: Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- Função D3D12DecomposeSubresource
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793656"
---
# <a name="d3d12decomposesubresource-function"></a>Função D3D12DecomposeSubresource

Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado.

## <a name="syntax"></a>Sintaxe


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sub-recurso* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice do subrecurso.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número máximo de níveis de mipmap no subrecurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

</dd> <dt>

*MipSlice* \[ out, ref\]
</dt> <dd>

Tipo: **T**

Gera a fatia MIP que corresponde ao índice de subrecurso fornecido.

</dd> <dt>

*ArraySlice* \[ out, ref\]
</dt> <dd>

Tipo: **U**

Gera a fatia da matriz que corresponde ao índice de subrecurso fornecido.

</dd> <dt>

*PlaneSlice* \[ out, ref\]
</dt> <dd>

Tipo: **V**

Gera a fatia do plano que corresponde ao índice de subrecurso fornecido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função determina qual fatia MIP, fatia de matriz e fatia de plano correspondem a um determinado índice de subrecurso. Esse é um utilitário útil, embora seja específico ao C++.

Essa função é declarada da seguinte maneira, com parâmetros C++ modelos para tipos **T**, **U** e **V**:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)

[Sub-recursos](subresources.md)
