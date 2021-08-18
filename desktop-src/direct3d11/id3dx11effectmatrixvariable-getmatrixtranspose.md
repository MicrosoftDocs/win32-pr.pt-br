---
title: Método GetMatrixTranspose ID3DX11EffectMatrixVariable (D3dx11effect.h)
description: Transpor e obter uma matriz de ponto flutuante.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Método GetMatrixTranspose Direct3D 11
- Método GetMatrixTranspose Direct3D 11 , interface ID3DX11EffectMatrixVariable
- ID3DX11EffectMatrixVariable interface Direct3D 11 , método GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d2f04057dac5bc432cc3c6a9a3060654d8f6d181836823aa29f0a02f82f667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046174"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a>Método ID3DX11EffectMatrixVariable::GetMatrixTranspose

Transpor e obter uma matriz de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pdata* 
</dt> <dd>

Tipo: **\* float**

Um ponteiro para o primeiro elemento de uma matriz transposta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

A transposição de uma matriz reorganizará a ordem de dados da ordem da coluna de linha para a ordem da linha de coluna (ou vice-versa).

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

 

 





