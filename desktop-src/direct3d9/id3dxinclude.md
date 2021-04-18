---
description: ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para \# incluir diretivas durante a compilação do sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interface ID3DXInclude (D3DX9Shader. h)
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
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771475"
---
# <a name="id3dxinclude-interface"></a>Interface ID3DXInclude

ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para \# incluir diretivas durante a compilação do sombreador. Cada um dos métodos nesta interface deve ser implementado pelo usuário que, em seguida, será usado como retornos de chamada para o aplicativo quando ocorrer uma das seguintes ações:

-   Um sombreador HLSL que contém um \# include é compilado chamando uma das funções D3DXCompileShader \* \* \* .
-   Um sombreador de assembly \# incluído é montado chamando qualquer uma das \* \* \* funções D3DXAssembleShader.
-   Um efeito que contém uma \# inclusão é compilado pelo chamando qualquer uma das funções D3DXCreateEffect \* \* \* ou D3DXCreateEffectCompiler \* \* \* .

## <a name="members"></a>Membros

A interface **ID3DXInclude** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXInclude** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXInclude** tem esses métodos.



| Método                               | Descrição                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Fechar**](id3dxinclude--close.md) | Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .<br/>                             |
| [**Aberto**](id3dxinclude--open.md)   | Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .<br/> |



 

## <a name="remarks"></a>Comentários

Um usuário cria uma interface ID3DXInclude implementando uma classe derivada dessa interface e implementando todos os métodos de interface.

O tipo LPD3DXINCLUDE é definido como um ponteiro para essa interface.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
