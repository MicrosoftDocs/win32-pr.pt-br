---
title: Elemento ABSTRACT
description: O elemento ABSTRACT contém texto que descreve o elemento ASX, BANNER ou ENTRY associado.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Elemento ABSTRATO Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781065"
---
# <a name="abstract-element"></a>Elemento ABSTRACT

O elemento **abstract** contém texto que descreve o elemento **ASX**, **banner** ou **entry** associado.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                       |
|-----------|--------------------------------|
| Pai    | **ASX**, **entrada**, **faixa** |
| Filho     | Nenhum                           |



 

## <a name="remarks"></a>Comentários

Se esse elemento aparecer em um elemento **ASX** , o texto será exibido como uma dica de ferramenta quando o mouse passar sobre o título mostrar.

Se esse elemento aparecer dentro de um elemento de **entrada** , o texto será exibido como uma dica de ferramenta quando o mouse passar sobre o título do clipe.

Se esse elemento aparecer dentro de um elemento de **faixa** , o texto será exibido como uma dica de ferramenta para o gráfico de faixa.

Use apenas um elemento **abstract** por escopo. Somente o primeiro elemento **abstract** dentro do escopo de outro elemento é usado quando um arquivo de metarquivo é processado. Quaisquer elementos **abstratos** subsequentes nesse escopo são ignorados.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
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

 

 





