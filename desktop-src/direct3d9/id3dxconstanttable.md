---
description: A interface ID3DXConstantTable é usada para acessar a tabela de constantes. Esta tabela contém as variáveis que são usadas por sombreadores e efeitos de linguagem de alto nível.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interface ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765094"
---
# <a name="id3dxconstanttable-interface"></a>Interface ID3DXConstantTable

A interface ID3DXConstantTable é usada para acessar a tabela de constantes. Esta tabela contém as variáveis que são usadas por sombreadores e efeitos de linguagem de alto nível.

## <a name="members"></a>Membros

A interface **ID3DXConstantTable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXConstantTable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXConstantTable** tem esses métodos.



| Método                                                                                       | Descrição                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Obtém um ponteiro para o buffer que contém a tabela de constantes.<br/>                                                          |
| [**Getbuffersize**](id3dxconstanttable--getbuffersize.md)                                   | Obtém o tamanho do buffer da tabela de constantes.<br/>                                                                             |
| [**Getconstant**](id3dxconstanttable--getconstant.md)                                       | Obtém uma constante procurando seu índice.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Obtém uma constante procurando seu nome.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.<br/>                                              |
| [**Getconstantelement**](id3dxconstanttable--getconstantelement.md)                         | Obtém uma constante de uma matriz de constantes. Uma matriz é composta de elementos.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Obtém uma descrição da tabela de constantes.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Retorna o índice de amostra.<br/>                                                                                              |
| [**Setbool**](id3dxconstanttable--setbool.md)                                               | Define um valor booliano.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Define uma matriz de valores Boolianos.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Define as constantes para seus valores padrão. Os valores padrão são declarados nas declarações de variável no sombreador.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Define um número de ponto flutuante.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Define uma matriz de números de ponto flutuante.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Define um valor inteiro.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Define uma matriz de inteiros.<br/>                                                                                              |
| [**Setmatrix**](id3dxconstanttable--setmatrix.md)                                           | Define uma matriz nontransposed.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Define uma matriz de matrizes nontransposed.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Define uma matriz de ponteiros para matrizes nontransposed.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Define uma matriz transposeda.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Define uma matriz de matrizes transpostas.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Define uma matriz de ponteiros para matrizes transpostas.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Define o conteúdo do buffer para a tabela de constantes.<br/>                                                                  |
| [**Setvector**](id3dxconstanttable--setvector.md)                                           | Define um vetor 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Define uma matriz de vetores 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXCONSTANTTABLE é definido como um ponteiro para a interface **ID3DXConstantTable** .


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
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

 

 
