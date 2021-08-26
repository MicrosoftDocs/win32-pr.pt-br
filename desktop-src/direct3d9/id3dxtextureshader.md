---
description: A interface ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interface ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95e6a8feb35ea5d1e38a5cb63bb1379e4995e7562839cc1b582ee8efd8550212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846976"
---
# <a name="id3dxtextureshader-interface"></a>Interface ID3DXTextureShader

A interface ID3DXTextureShader.

## <a name="members"></a>Membros

A interface **ID3DXTextureShader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureShader** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXTextureShader** tem esses métodos.



| Método                                                                                       | Descrição                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**Getconstant**](id3dxtextureshader--getconstant.md)                                       | Obtém uma constante procurando seu índice.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Obter um ponteiro para a tabela de constantes.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Obtém uma constante procurando seu nome.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Obtém um ponteiro para a matriz de constantes na tabela de constantes.<br/>  |
| [**Getconstantelement**](id3dxtextureshader--getconstantelement.md)                         | Obtenha uma constante da tabela de constantes.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Obtém uma descrição da tabela de constantes.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Obtém um ponteiro para a função de fluxo DWORD.<br/>                     |
| [**Setbool**](id3dxtextureshader--setbool.md)                                               | Define um valor BOOL.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Define uma matriz de valores BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Define as constantes para os valores padrão declarados no sombreador.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Define um número de ponto flutuante.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Define uma matriz de números de ponto flutuante.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Define um valor inteiro.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Define uma matriz de inteiros.<br/>                                       |
| [**Setmatrix**](id3dxtextureshader--setmatrix.md)                                           | Define uma matriz não transposeda.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Define uma matriz de matrizes não transpostas.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Define uma matriz de ponteiros para matrizes não transpostas.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Define uma matriz transposeda.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Define uma matriz de matrizes transpostas.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Define uma matriz de ponteiros para matrizes transpostas.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Define a tabela constante com os dados no buffer.<br/>             |
| [**Setvector**](id3dxtextureshader--setvector.md)                                           | Define um vetor 4D.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Define uma matriz de vetores 4D.<br/>                                     |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXTextureShader** é obtida chamando a função [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .

A interface **ID3DXTextureShader** , como todas as interfaces com, herda a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

O tipo LPD3DXTEXTURESHADER é definido como um ponteiro para a interface **ID3DXTextureShader** .


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
