---
description: Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Método ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761215"
---
# <a name="id3dxincludeopen-method"></a>Método ID3DXInclude:: Open

Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Incluir* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md)**

O local do \# arquivo de inclusão. Consulte [**\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do \# arquivo de inclusão.

</dd> <dt>

*pParentData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o contêiner que inclui o \# arquivo de inclusão. O compilador pode passar nulo em *pParentData*. Para obter mais informações, consulte a seção "procurando arquivos de inclusão" em [compilar um efeito (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ppData* \[ fora\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Ponteiro para o buffer retornado que contém as diretivas include. Esse ponteiro permanece válido até que [**ID3DXInclude:: Close**](id3dxinclude--close.md) seja chamado.

</dd> <dt>

*pBytes* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de bytes retornados em ppData.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao ler o \# arquivo de inclusão, a API que causou o retorno de chamada será reprovada. Ele é um dos seguintes:

-   O sombreador HLSL falhará em uma das funções do D3DXCompileShader \* \* \* .
-   O sombreador de assembly falhará em uma das \* \* \* funções D3DXAssembleShader.
-   O efeito falhará em uma das \* \* \* funções D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: fechar**](id3dxinclude--close.md)
</dt> </dl>

 

 
