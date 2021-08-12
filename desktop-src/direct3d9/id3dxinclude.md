---
description: ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para diretivas de inclusão durante a \# compilação do sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interface ID3DXInclude (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e48ab32894ad1bf4c2f992ab4fff5953b3d98de4afd5e044de0119e056ee8133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295176"
---
# <a name="id3dxinclude-interface"></a>Interface ID3DXInclude

ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para diretivas de inclusão durante a \# compilação do sombreador. Cada um dos métodos nessa interface deve ser implementado pelo usuário, que será usado como retornos de chamada para o aplicativo quando ocorrer um dos seguintes:

-   Um sombreador HLSL que contém uma inclusão é compilado chamando uma das \# funções D3DXCompileShader. \* \* \*
-   Uma inclusão de sombreador de assembly é montada chamando qualquer uma \# das funções D3DXAssembleShader. \* \* \*
-   Um efeito que contém uma inclusão é compilado chamando qualquer uma das funções \# D3DXCreateEffect ou \* \* \* D3DXCreateEffectCompiler. \* \* \*

## <a name="members"></a>Membros

A interface **ID3DXInclude** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXInclude** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXInclude** tem esses métodos.



| Método                               | Descrição                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Perto**](id3dxinclude--close.md) | Um método implementado pelo usuário para fechar um arquivo de \# inclusão de sombreador.<br/>                             |
| [**Aberto**](id3dxinclude--open.md)   | Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de \# inclusão de sombreador.<br/> |



 

## <a name="remarks"></a>Comentários

Um usuário cria uma interface ID3DXInclude implementando uma classe que deriva dessa interface e implementando todos os métodos de interface.

O tipo LPD3DXINCLUDE é definido como um ponteiro para essa interface.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
