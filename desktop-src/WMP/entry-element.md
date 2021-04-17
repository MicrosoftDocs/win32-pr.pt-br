---
title: Elemento ENTRY
description: O elemento ENTRY especifica um arquivo de mídia do Windows para renderizar como um clipe.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento de entrada Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758215"
---
# <a name="entry-element"></a>Elemento ENTRY

O elemento **entry** especifica um arquivo de mídia do Windows para renderizar como um clipe.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Atributos

**CLIENTSKIP**

Valor que indica se o usuário pode pular para a frente do clipe.

Os possíveis valores incluem os seguintes.



| Valor | Descrição                                   |
|-------|-----------------------------------------------|
| YES   | Padrão. O usuário pode pular o clipe para frente. |
| Não    | O usuário não pode pular o clipe para frente.       |



 

**SKIPIFREF**

Valor que indica se o Windows Media Player deve ignorar esse clipe quando o elemento de **entrada** é incluído em um segundo metarquivo por meio do uso de um elemento **ENTRYREF** .

Os possíveis valores incluem os seguintes.



| Valor | Descrição                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | O Windows Media Player irá ignorar essa entrada, se for referenciada por meio de um elemento **ENTRYREF** . |
| Não    | Padrão. O Windows Media Player não ignorará essa entrada.                                   |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai | **ASX**, **evento**, **repetir**                                                                                                                                                               |
| Elementos filho  | **abstrato**, **autor**, **faixa**, **base**, **direitos autorais**,  **duração**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title** |



 

## <a name="remarks"></a>Comentários

Esse elemento é a construção fundamental em um metarquivo do Windows Media. O elemento **entry** e seus atributos associados definem meta-informações para uma única parte lógica de conteúdo, chamada de clipe. Elementos filho dentro do escopo de um elemento de **entrada** definem o conteúdo de mídia para o Windows Media Player abrir (**ref**), informações sobre o clipe que o Windows Media Player exibirá como texto (**autor**, **direitos autorais**, **título**) e outras configurações relacionadas ao clipe. O elemento filho **ref** vincula o conteúdo a ser transmitido para o elemento de **entrada** pai. Embora o script não seja interrompido, a **entrada** não faz sentido sem um filho de **referência** .

Se o valor do atributo **CLIENTSKIP** for no, o usuário não poderá pular para frente a parte do conteúdo definido pelo elemento de **entrada** . Isso não funcionará se o elemento de **referência** filho fizer referência a outro metarquivo. Os metaarquivos aninhados devem ser referenciados usando o elemento **ENTRYREF** .

O atributo **SKIPIFREF** pertence apenas aos elementos de **entrada** que são incluídos em um segundo metarquivo por meio do uso de um elemento **ENTRYREF** . O elemento **ENTRYREF** faz referência a outro metarquivo para inclusão lógica no arquivo atual. Se o valor do atributo **SKIPIFREF** para um elemento de **entrada** do arquivo de METARQUIVO referenciado for sim, o Windows Media Player ignorará essa entrada retirada e passará para o próximo elemento de **entrada** , se houver. O próximo elemento de **entrada** pode ser a entrada seguinte no arquivo original ou a entrada seguinte no metarquivo referenciado no elemento **ENTRYREF** .

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
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

 

 





