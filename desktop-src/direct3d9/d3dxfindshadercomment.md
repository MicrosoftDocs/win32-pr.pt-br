---
description: Pesquisa em um sombreador um comentário específico. O comentário é identificado por um código de quatro caracteres (FOURCC) na primeira DWORD do comentário.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Função D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771641"
---
# <a name="d3dxfindshadercomment-function"></a>Função D3DXFindShaderComment

Pesquisa em um sombreador um comentário específico. O comentário é identificado por um código de quatro caracteres (FOURCC) na primeira DWORD do comentário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para o fluxo DWORD da função de sombreador.

</dd> <dt>

*FOURCC* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Código FOURCC que identifica o bloco de comentários. Consulte [formatos FOURCC](d3dformat.md).

</dd> <dt>

*ppData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Retorna um ponteiro para os dados de comentário (sem incluir o token de comentário e o código FOURCC). Esse valor pode ser **nulo**.

</dd> <dt>

*pSizeInBytes* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Retorna o tamanho dos dados de comentário em bytes. Esse valor pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se o comentário não for encontrado e nenhum outro erro tiver ocorrido, S \_ false será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
