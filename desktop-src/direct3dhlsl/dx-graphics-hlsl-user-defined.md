---
title: Tipo definido pelo usuário
description: Use a sintaxe a seguir para declarar um tipo definido pelo usuário.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee73cd5afcda15bcc821d7fea5b648924829d483a33b9c67c140eed0b100e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789306"
---
# <a name="user-defined-type"></a>Tipo definido pelo usuário

Use a sintaxe a seguir para declarar um tipo definido pelo usuário.



|                                           |
|-------------------------------------------|
| **\[ \] \[ índice \] de nome de tipo de constante** de typedef; |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[const\]**<br/>                 | Opcional. Essa palavra-chave marca explicitamente o tipo como uma constante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**<br/>     | Identifica o tipo de dados; deve ser um dos tipos de dados intrínsecos HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**<br/> | Tamanho de matriz opcional. Deve ser um inteiro sem sinal entre 1 e 4, inclusive.<br/> |



 

Além dos tipos de dados intrínsecos internos, o HLSL dá suporte a tipos definidos pelo usuário ou personalizados que seguem essa sintaxe:

## <a name="remarks"></a>Comentários

Os tipos definidos pelo usuário não diferenciam maiúsculas de minúsculas. Para sua conveniência, os tipos a seguir são definidos automaticamente em escopo superglobal.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



O sinal de sustenido ( \# ) representa um dígito inteiro entre 1 e 4.

Para compatibilidade com os efeitos do DirectX 8, os seguintes tipos são definidos automaticamente em escopo superglobal:


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





