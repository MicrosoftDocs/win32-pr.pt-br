---
title: Método ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect.h)
description: Definir uma matriz de matrizes de ponto flutuante.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Método SetMatrixArray Direct3D 11
- Método SetMatrixArray Direct3D 11 , interface ID3DX11EffectMatrixVariable
- ID3DX11EffectMatrixVariable interface Direct3D 11 , método SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c310dcb5d5469edd603b4d8801eed91366b68fbe9a25b089075d4bb8118a811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046084"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a>Método ID3DX11EffectMatrixVariable::SetMatrixArray

Definir uma matriz de matrizes de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pdata* 
</dt> <dd>

Tipo: **\* float**

Um ponteiro para a primeira matriz.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos de matriz a ignorar desde o início da matriz.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos a definir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

