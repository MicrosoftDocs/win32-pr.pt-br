---
title: Elemento BASE
description: O elemento BASE define uma cadeia de caracteres de URL anexada à frente das URLs enviadas ao Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Elemento BASE Windows Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760894"
---
# <a name="base-element"></a>Elemento BASE

O elemento **base** define uma cadeia de caracteres de URL anexada à frente das URLs enviadas ao Windows Media Player.

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

A cadeia de caracteres anexada à frente às URLs enviadas ao Windows Media Player. O valor padrão é a cadeia de caracteres nula ("").

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **ASX**, **entrada** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma cadeia de caracteres de URL anexada à frente das URLs de flip URL enviadas ao Windows Media Player. A inversão de URL é um mecanismo de script que faz com que o Windows Media Player abra uma nova URL em um navegador ou quadro de navegador quando recebe um comando de script.

O elemento **base** é semelhante a um diretório base para links relativos. Ele afeta apenas as URLs enviadas usando comandos de script como parte do fluxo de conteúdo que está sendo executado no Windows Media Player.

Um elemento **base** definido como o filho de um elemento **ASX** torna-se o padrão para todo o metarquivo. Um elemento **base** definido em um elemento de **entrada** substitui qualquer elemento **base** no elemento pai **ASX** (somente para esse elemento de **entrada** ).

> [!Note]  
> Se o atributo **href** não terminar com um caractere/, o Windows Media Player acrescentará um ao final da cadeia de caracteres.

 

## <a name="examples"></a>Exemplos


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





