---
title: Interface ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Uma interface de matriz-variável acessa uma matriz.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interface ID3DX11EffectMatrixVariable Direct3D 11
- Interface ID3DX11EffectMatrixVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968637"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>Interface ID3DX11EffectMatrixVariable

Uma interface de matriz-variável acessa uma matriz.

## <a name="members"></a>Membros

A interface **ID3DX11EffectMatrixVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectMatrixVariable** tem esses métodos.



| Método                                                                                 | Descrição                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Getmatrix**](id3dx11effectmatrixvariable-getmatrix.md)                             | Obter uma matriz.<br/>                                          |
| [**GetMatrixArray**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Obtenha uma matriz de matrizes.<br/>                              |
| [**GetMatrixTranspose**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Transpor e obter uma matriz de ponto flutuante.<br/>             |
| [**GetMatrixTransposeArray**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Transpor e obter uma matriz de matrizes de ponto flutuante.<br/> |
| [**Setmatrix**](id3dx11effectmatrixvariable-setmatrix.md)                             | Defina uma matriz de ponto flutuante.<br/>                           |
| [**SetMatrixArray**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Defina uma matriz de matrizes de ponto flutuante.<br/>               |
| [**SetMatrixTranspose**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Transpor e definir uma matriz de ponto flutuante.<br/>             |
| [**SetMatrixTransposeArray**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Transpor e definir uma matriz de matrizes de ponto flutuante.<br/> |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





