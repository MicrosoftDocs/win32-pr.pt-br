---
title: Elemento ENTRYREF
description: O elemento ENTRYREF aponta para os elementos de entrada em um metarquivo externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF do Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789557"
---
# <a name="entryref-element"></a>Elemento ENTRYREF

O elemento **ENTRYREF** aponta para os elementos de **entrada** em um metarquivo externo.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para um metarquivo referenciado.

**CLIENTBIND**

Não há mais suporte para este atributo.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                       |
|-----------------|--------------------------------|
| Elementos pai | **ASX**, **evento**, **repetir** |
| Elementos filho  | Nenhum                           |



 

## <a name="remarks"></a>Comentários

Esse elemento aponta para o conteúdo de um metarquivo externo. O Windows Media Player processa os elementos de **entrada** do metarquivo referenciado como se eles estivessem incluídos no metarquivo primário na posição do elemento **ENTRYREF** . No entanto, ele ignora todos os elementos de **entrada** no metarquivo referenciado que têm o atributo **SKIPIFREF** definido como Sim.

O Windows Media Player 7,0, 7,1 e Windows Media Player para Windows XP ignoram todos os elementos **ENTRYREF** no metarquivo referenciado. Portanto, os metaarquivos só podem ser aninhados em um nível profundo ao usar essas versões do Player. O Windows Media Player também ignora o elemento **ASX** no arquivo referenciado junto com seus atributos. O Windows Media Player 9 Series ou posterior dá suporte ao aninhamento de metaarquivos de até cinco níveis de profundidade.

A URL especificada no atributo **href** torna-se a URL base para quaisquer URLs relativas no metarquivo externo. Essa URL é usada quando uma entrada do metarquivo externo está sendo executada e o usuário a adiciona à biblioteca.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





