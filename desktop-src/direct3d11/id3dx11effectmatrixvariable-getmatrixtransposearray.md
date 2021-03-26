---
title: Método ID3DX11EffectMatrixVariable GetMatrixTransposeArray (D3dx11effect. h)
description: Transpor e obter uma matriz de matrizes de ponto flutuante.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Método GetMatrixTransposeArray Direct3D 11
- Método GetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968602"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a>Método ID3DX11EffectMatrixVariable:: GetMatrixTransposeArray

Transpor e obter uma matriz de matrizes de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Um ponteiro para o primeiro elemento de uma matriz das matrizes tranposed.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O deslocamento (em número de matrizes) entre o início da matriz e a primeira matriz a ser obtida.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de matrizes na matriz a serem obtidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

A transposição de uma matriz reorganizará a ordem dos dados da ordem da coluna de linha para a ordem da linha de coluna (ou vice-versa).

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

