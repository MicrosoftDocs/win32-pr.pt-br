---
title: Elemento EVENT (SDK do WMP)
description: O elemento EVENT define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Elemento de evento Windows Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760262"
---
# <a name="event-element"></a>Elemento EVENT

O elemento **Event** define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Atributos

**Nome** (obrigatório)

O nome do evento.

**WHENDONE** (obrigatório)

Um valor que define o que o Windows Media Player faz depois de reproduzir o conteúdo referenciado.

Os valores a seguir são possíveis.



| Valor  | Descrição                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | A entrada atual (o clipe interrompido pelo evento) reinicia a reprodução. Se o conteúdo for armazenado no conteúdo, ele será retomado no mesmo ponto em que foi interrompido; Se o conteúdo for difundido, ele será retomado na posição atual.        |
| NEXT   | O próximo elemento de **entrada** é reproduzido como se o evento não tivesse ocorrido e o Windows Media Player atingiu o final do clipe atual.                                                                                             |
| BREAK  | Se a entrada atual estiver dentro de um loop de **repetição** , o loop será encerrado como se a contagem de repetição tivesse sido concluída. Caso contrário, o Windows Media Player vai até o final da lista de reprodução como se a entrada final tivesse sido concluída como de costume. |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                |
|-----------------|-------------------------|
| Elementos pai | **ASX**                 |
| Elementos filho  | **entrada**, **ENTRYREF** |



 

## <a name="remarks"></a>Comentários

Esse elemento define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento. Um evento é um tipo específico de comando de script inserido em um fluxo enviado ao Windows Media Player que consiste em uma cadeia de caracteres dupla. A primeira cadeia de caracteres é a palavra "Event", e a segunda cadeia de caracteres é o nome do evento. O nome do evento na segunda cadeia de caracteres deve corresponder ao nome do evento definido no metarquivo. (A correspondência não diferencia maiúsculas de minúsculas.) Os eventos podem ser enviados para o Windows Media Player recebendo um fluxo em tempo real ou podem ser salvos em um arquivo. ASF,. WMA ou. wmv que é entregue como um fluxo unicast sob demanda. Quando o Windows Media Player recebe o comando de script, ele processa o evento conforme definido pelo elemento **Event** .

Esse elemento define um escopo de elementos **entry** ou **ENTRYREF** que são processados sempre que o Windows Media Player recebe o comando de script com o evento nomeado. O **ENTRYREF** pode ser uma URL que aponta para uma página ASP. Com esse elemento, você pode especificar um comportamento para a alternância de fluxo quase em tempo real, em oposição às alterações de fluxo pré-autorizadas usando referências a outras partes de conteúdo ou os metaarquivos de mídia do Windows.

Ao usar páginas ASP para gerar listas de reprodução, você deve especificar um valor para a *resposta*. Propriedade **ContentType** e a *resposta*. **expira** a propriedade na página ASP devido a problemas de latência com o Windows Media Player. A *resposta*. **ContentType** deve ser uma extensão de nome de arquivo válida para os metaarquivos de mídia do Windows. Os tipos válidos incluem. ASF,. ASX,. WMA,. Wax,. wmv e. wvx.

Consulte o SDK da plataforma para obter detalhes sobre como usar o objeto de **resposta** no ASP.

Esse elemento pode aparecer em qualquer lugar dentro do elemento **ASX** . Se vários elementos de **evento** dentro de um elemento **ASX** tiverem valores idênticos para seus atributos de **nome** , o Windows Media Player usará a primeira ocorrência dentro do elemento **ASX** e ignorará todos os outros. Quando elementos de **evento** têm atributos de **nome** distintos, sua ordem dentro do elemento **ASX** não importa.

O Windows Media Player descarta eventos recebidos durante o processamento de outro evento. Não há suporte para o aninhamento de eventos. Quando o Windows Media Player está no modo de visualização, o conteúdo do evento não é restrito pelo elemento **PREVIEWDURATION** ; o comprimento total do conteúdo do evento pode ser reproduzido mesmo se a duração da visualização do elemento de **entrada** ativo expirar antes do final do evento.

## <a name="examples"></a>Exemplos

Neste exemplo, quando o Windows Media Player recebe o evento de comando de script e a cadeia de caracteres de comando "Adlink" na mídia de streaming que está renderizando, ele pesquisa na lista de reprodução um **EventName** "Adlink". O Windows Media Player alterna do fluxo que está renderizando e reproduz o conteúdo referenciado no **evento**" https://example.microsoft.com/adlink.htm ".

O atributo de **entrada** **CLIENTSKIP** está definido como não para impedir que o clipe de **evento** seja ignorado. Ele deve ser reproduzido.

O script `WHENDONE="RESUME"` instrui o Windows Media Player a retomar a reprodução da mídia anterior que ele alternou assim que Adlink. ASF for concluído.


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
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
</dt> <dt>

[**Modelo de objeto do Windows Media Player**](windows-media-player-object-model.md)
</dt> </dl>

 

 





