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
ms.openlocfilehash: 153759dbe4bef47693cba13549b58215e4992686eab81cdcb4dadb33aa30279f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903046"
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

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metarquivo de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





