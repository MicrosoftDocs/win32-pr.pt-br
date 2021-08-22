---
description: Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Método ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 32df78aedcf4e7e229eec8c9648c82c86f6fea9f4c7176b8780cee67ccf49fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987396"
---
# <a name="id3dxincludeclose-method"></a>Método ID3DXInclude:: Close

Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o buffer retornado que contém as diretivas include. Esse é o ponteiro retornado pela chamada [**ID3DXInclude:: Open**](id3dxinclude--open.md) correspondente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao ler o \# arquivo de inclusão, a API que causou o retorno de chamada será reprovada. Ele é um dos seguintes:

-   O sombreador HLSL falhará em uma das funções do D3DXCompileShader \* \* \* .
-   O sombreador de assembly falhará em uma das \* \* \* funções D3DXAssembleShader.
-   O efeito falhará em uma das \* \* \* funções D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .

## <a name="remarks"></a>Comentários

Se [**ID3DXInclude:: Open**](id3dxinclude--open.md) tiver sido bem-sucedido, **ID3DXInclude:: Close** terá a garantia de ser chamado antes que a API que usa essa interface retorne.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: abrir**](id3dxinclude--open.md)
</dt> </dl>

 

 
