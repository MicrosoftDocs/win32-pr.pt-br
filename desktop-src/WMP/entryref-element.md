---
title: Elemento ENTRYREF
description: O elemento ENTRYREF aponta para os elementos ENTRY em um metadado externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61fa3403fc56c6a02f97330b3c2f62d1c3e3c723f50672520ea42fb4a2018705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996665"
---
# <a name="entryref-element"></a>Elemento ENTRYREF

O **elemento ENTRYREF** aponta para os **elementos ENTRY** em um metadado externo.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obrigatório)

URL para um metadado referenciado.

**CLIENTBIND**

Não há mais suporte para este atributo.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                       |
|-----------------|--------------------------------|
| Elementos pai | **ASX,** **EVENT,** **REPEAT** |
| Elementos filho  | Nenhum                           |



 

## <a name="remarks"></a>Comentários

Esse elemento aponta para o conteúdo de um metadado externo. Windows Media Player processa os elementos **ENTRY** do metadado referenciado como se eles fossem incluídos no metadado primário na posição do **elemento ENTRYREF.** No entanto, ele ignora todos **os elementos ENTRY** no metadado referenciado que têm o atributo **SKIPIFREF** definido como YES.

Windows Media Player 7.0, 7.1 e Windows Media Player para Windows XP ignoram quaisquer elementos **ENTRYREF** no metadado referenciado. Portanto, os metadados só podem ser aninhados em um nível profundo ao usar essas versões do Player. Windows Media Player também ignora o **elemento ASX** no arquivo referenciado junto com seus atributos. Windows Media Player Série 9 ou posterior dá suporte ao aninhamento de metadados de até cinco níveis de profundidade.

A URL especificada no atributo **HREF** se torna a URL base para todas as URLs relativas no metadado externo. Essa URL é usada quando uma entrada do metadado externo está sendo reprodução e o usuário a adiciona à biblioteca.

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

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





