---
description: Fornece métodos para obter e definir parâmetros de efeito, como constantes, funções, sombreadores e técnicas.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: Interface ID3DXBaseEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e72fabf7db8341821885afb160fa73cb0fc9f395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091955"
---
# <a name="id3dxbaseeffect-interface"></a>Interface ID3DXBaseEffect

Fornece métodos para obter e definir parâmetros de efeito, como constantes, funções, sombreadores e técnicas.

## <a name="members"></a>Membros

A interface **ID3DXBaseEffect** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseEffect** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXBaseEffect** tem esses métodos.



| Método                                                                                    | Descrição                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | Obtém o identificador de uma anotação. <br/>                                                                                                                                                                                     |
| [**GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md)                       | Obtém o identificador de uma anotação pesquisando seu nome.<br/>                                                                                                                                                               |
| [**Getbool**](id3dxbaseeffect--getbool.md)                                               | Obtém um valor BOOL.<br/>                                                                                                                                                                                                     |
| [**GetBoolArray**](id3dxbaseeffect--getboolarray.md)                                     | Obtém uma matriz de valores BOOL.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Obtém a descrição do efeito.<br/>                                                                                                                                                                                           |
| [**GetFloat**](id3dxbaseeffect--getfloat.md)                                             | Obtém um valor de ponto flutuante.<br/>                                                                                                                                                                                           |
| [**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)                                   | Obtém uma matriz de valores de ponto flutuante.<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | Obtém o identificador de uma função.<br/>                                                                                                                                                                                         |
| [**GetFunctionByName**](id3dxbaseeffect--getfunctionbyname.md)                           | Obtém o identificador de uma função procurando seu nome.<br/>                                                                                                                                                                  |
| [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)                               | Obtém uma descrição da função.<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | Obtém um inteiro.<br/>                                                                                                                                                                                                       |
| [**GetIntArray**](id3dxbaseeffect--getintarray.md)                                       | Obtém uma matriz de inteiros.<br/>                                                                                                                                                                                             |
| [**Getmatrix**](id3dxbaseeffect--getmatrix.md)                                           | Obtém uma matriz nontransposed.<br/>                                                                                                                                                                                           |
| [**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)                                 | Obtém uma matriz de matrizes nontransposed.<br/>                                                                                                                                                                               |
| [**GetMatrixPointerArray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Obtém uma matriz de ponteiros para matrizes nontransposed.<br/>                                                                                                                                                                   |
| [**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)                         | Obtém uma matriz transposeda.<br/>                                                                                                                                                                                              |
| [**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)               | Obtém uma matriz de matrizes transpostas.<br/>                                                                                                                                                                                  |
| [**GetMatrixTransposePointerArray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Obtém uma matriz de ponteiros para matrizes transpostas.<br/>                                                                                                                                                                      |
| [**GetParameter**](id3dxbaseeffect--getparameter.md)                                     | Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura.<br/>                                                                                                                                              |
| [**GetParameterByName**](id3dxbaseeffect--getparameterbyname.md)                         | Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura procurando seu nome.<br/>                                                                                                                       |
| [**GetParameterBySemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura pesquisando sua semântica com uma pesquisa que não diferencia maiúsculas de minúsculas.<br/>                                                                                    |
| [**GetParameterDesc**](id3dxbaseeffect--getparameterdesc.md)                             | Obtém uma descrição de parâmetro ou anotação.<br/>                                                                                                                                                                            |
| [**ParameterElement**](id3dxbaseeffect--getparameterelement.md)                       | Obtenha o identificador de um parâmetro de elemento de matriz.<br/>                                                                                                                                                                          |
| [**Getpass**](id3dxbaseeffect--getpass.md)                                               | Obtém o identificador de uma passagem.<br/>                                                                                                                                                                                             |
| [**GetPassByName**](id3dxbaseeffect--getpassbyname.md)                                   | Obtém o identificador de uma passagem procurando seu nome.<br/>                                                                                                                                                                      |
| [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)                                       | Obtém uma descrição de passagem.<br/>                                                                                                                                                                                               |
| [**GetPixelShader**](id3dxbaseeffect--getpixelshader.md)                                 | Obtém um sombreador de pixel.<br/>                                                                                                                                                                                                   |
| [**GetString**](id3dxbaseeffect--getstring.md)                                           | Obtém uma cadeia de caracteres.<br/>                                                                                                                                                                                                         |
| [**Gettécnica**](id3dxbaseeffect--gettechnique.md)                                     | Obtém o identificador de uma técnica.<br/>                                                                                                                                                                                        |
| [**GetTechniqueByName**](id3dxbaseeffect--gettechniquebyname.md)                         | Obtém o identificador de uma técnica pesquisando seu nome.<br/>                                                                                                                                                                 |
| [**GetTechniqueDesc**](id3dxbaseeffect--gettechniquedesc.md)                             | Obtém uma descrição técnica.<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | Obtém uma textura.<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | Obtenha o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas. Esse método pode ser usado no lugar de quase todas as chamadas GetXXX em **ID3DXBaseEffect**.<br/> |
| [**Getvector**](id3dxbaseeffect--getvector.md)                                           | Obtém um vetor.<br/>                                                                                                                                                                                                         |
| [**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)                                 | Obtém uma matriz de vetores.<br/>                                                                                                                                                                                              |
| [**GetVertexShader**](id3dxbaseeffect--getvertexshader.md)                               | Obtém um sombreador de vértice.<br/>                                                                                                                                                                                                  |
| [**SetArrayRange**](id3dxbaseeffect--setarrayrange.md)                                   | Defina o intervalo de uma matriz para passar para o dispositivo.<br/>                                                                                                                                                                       |
| [**Setbool**](id3dxbaseeffect--setbool.md)                                               | Define um valor BOOL.<br/>                                                                                                                                                                                                     |
| [**SetBoolArray**](id3dxbaseeffect--setboolarray.md)                                     | Define uma matriz de valores Boolianos.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Define um valor de ponto flutuante.<br/>                                                                                                                                                                                           |
| [**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)                                   | Define uma matriz de valores de ponto flutuante.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Define um número inteiro.<br/>                                                                                                                                                                                                       |
| [**SetIntArray**](id3dxbaseeffect--setintarray.md)                                       | Define uma matriz de inteiros.<br/>                                                                                                                                                                                             |
| [**Setmatrix**](id3dxbaseeffect--setmatrix.md)                                           | Define uma matriz não transposeda.<br/>                                                                                                                                                                                          |
| [**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)                                 | Define uma matriz de matrizes nontransposed.<br/>                                                                                                                                                                               |
| [**SetMatrixPointerArray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Define uma matriz de ponteiros para matrizes nontransposed.<br/>                                                                                                                                                                   |
| [**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)                         | Define uma matriz transposeda.<br/>                                                                                                                                                                                              |
| [**SetMatrixTransposeArray**](id3dxbaseeffect--setmatrixtransposearray.md)               | Define uma matriz de matrizes transpostas.<br/>                                                                                                                                                                                  |
| [**SetMatrixTransposePointerArray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Define uma matriz de ponteiros para matrizes transpostas.<br/>                                                                                                                                                                      |
| [**SetString**](id3dxbaseeffect--setstring.md)                                           | Define uma cadeia de caracteres.<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | Define uma textura.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Defina o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas. <br/>                                                                                        |
| [**Setvector**](id3dxbaseeffect--setvector.md)                                           | Define um vetor.<br/>                                                                                                                                                                                                         |
| [**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)                                 | Define uma matriz de vetores.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXBASEEFFECT é definido como um ponteiro para essa interface.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
