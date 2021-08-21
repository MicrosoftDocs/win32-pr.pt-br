---
title: Função D3D12DecomposeSubresource (D3dx12.h)
description: Saída da fatia mip, da fatia da matriz e da fatia do plano que correspondem ao índice de sub-fonte especificado.
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
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045634"
---
# <a name="d3d12decomposesubresource-function"></a>Função D3D12DecomposeSubresource

Saída da fatia mip, da fatia da matriz e da fatia do plano que correspondem ao índice de sub-fonte especificado.

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

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O índice da sub-fonte.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número máximo de níveis de mipmap na sub-fonte.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

</dd> <dt>

*MipSlice* \[ out, ref\]
</dt> <dd>

Tipo: **T**

Saída da fatia mip que corresponde ao índice de sub-fonte determinado.

</dd> <dt>

*ArraySlice* \[ out, ref\]
</dt> <dd>

Tipo: **U**

Saída da fatia da matriz que corresponde ao índice de sub-fonte determinado.

</dd> <dt>

*PlaneSlice* \[ out, ref\]
</dt> <dd>

Tipo: **V**

Saída da fatia do plano que corresponde ao índice de sub-fonte determinado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função determina qual fatia mip, fatia de matriz e fatia de plano correspondem a um determinado índice de sub-recursos. Esse é um utilitário útil, embora seja específico do C++.

Essa função é declarada da seguinte forma, com parâmetros templatized C++ para os tipos **T,** **U** e **V:**


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
| parâmetro<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)

[Sub-recursos](subresources.md)
