---
title: Método setmatrix ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Defina uma matriz de ponto flutuante.
ms.assetid: 91c69bc0-c8c6-4232-8c70-801ac8ddbcda
keywords:
- Método setmatrix Direct3D 11
- Método setmatrix Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, método setmatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b302c4506a0449fe9c0aa83b06b2b47c902fe6302a05d6f576fa42ab8ac676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046094"
---
# <a name="id3dx11effectmatrixvariablesetmatrix-method"></a>Método ID3DX11EffectMatrixVariable:: setmatrix

Defina uma matriz de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrix(
   float *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Um ponteiro para o primeiro elemento na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

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

 

 





