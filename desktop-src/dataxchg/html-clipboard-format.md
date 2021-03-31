---
title: Formato de área de transferência HTML
description: Esta seção discute o formato de área de transferência HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interface do usuário do Windows, área de transferência
- área de transferência, recortando dados
- área de transferência, copiando dados
- área de transferência, colando dados
- área de transferência, formatos
- área de transferência, formato HTML
- área de transferência, cortando texto em HTML
- área de transferência, colando texto HTML
- Formato de área de transferência CF_HTML
- área de transferência, formato de CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005691"
---
# <a name="html-clipboard-format"></a>Formato de área de transferência HTML

Os requisitos para transferir texto HTML por meio da área de transferência diferem de acordo com o cenário. Este artigo se preocupa com a recorte e colagem de fragmentos de um documento HTML. Pode haver requisitos para transferir documentos HTML inteiros por meio da área de transferência; no entanto, este artigo é orientado por um requisito para transferir fragmentos de texto HTML selecionado. Dessa forma, um método que exigia que todo o documento HTML fosse copiado para a área de transferência é visto como muito pesado.

O \_ formato de área de transferência HTML do CF permite que um fragmento de texto HTML bruto e seu contexto sejam armazenados na área de transferência como ASCII. Isso permite que o contexto do fragmento HTML, que consiste em todas as marcas adjacentes anteriores, seja examinado por um aplicativo para que as marcas ao redor do fragmento HTML possam ser observadas com seus atributos. Embora seja preciso que os aplicativos decidam como interpretar esses fragmentos, algumas diretrizes básicas são incluídas aqui com base nas implementações de IE4/MSHTML.

O nome oficial da área de transferência (a cadeia de caracteres usada por RegisterClipboardFormat) é o formato HTML.

-   [Descrição](#description)
-   [Cenários](#scenarios)

## <a name="description"></a>Descrição

\_O HTML do CF é totalmente um formato de texto (para ser, entre outras coisas, no espírito HTML, e usa UTF-8) e inclui um `description` , um opcional `context` e, dentro do contexto, o `fragment` .

Veja a seguir um exemplo de uma área de transferência:


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



A descrição inclui o número de versão da área de transferência e os deslocamentos, indicando onde o contexto e o início e término do fragmento. A descrição é uma lista de palavras-chave de texto ASCII (min/Maj não é significativa) seguida por uma cadeia de caracteres e separados por dois-pontos (:).

**Versão**: VV número de versão da área de transferência. A versão inicial é 0,9.

**StartHTML**: byteCount desde o início da área de transferência até o início do contexto, ou-1 se nenhum contexto.

**Endhtml**: byteCount desde o início da área de transferência até o final do contexto, ou-1, se não houver nenhum contexto.

**StartFragment**: byteCount desde o início da área de transferência até o início do fragmento.

**EndFragment**: byteCount desde o início da área de transferência até o fim do fragmento.

**StartSelection**: byteCount desde o início da área de transferência até o início da seleção.

**Endselecting**: byteCount desde o início da área de transferência até o fim da seleção.

As palavras-chave StartSelection e endseleções são opcionais e devem ser omitidas se você não quiser que o aplicativo gere essas informações.

Outras informações desse tipo podem ser adicionadas aqui mais tarde, pois o HTML começa no StartHTMLoffset. Por exemplo, vários pares de StartFragment/endfrager podem ser adicionados posteriormente para dar suporte à seleção não contígua de fragmentos.

Para a conveniência dos programas que geram os bytecounts, os bytecounts podem ser preenchidos por zeros. Por exemplo, os programas que geram os bytecounts poderiam afetar arbitrariamente dez (10) zeros para cada palavra-chave (StartHTML: 0000000000) e, em seguida, quando o StartHTML byteCount exato é conhecido (digamos, 71), o programa pode substituir o número apropriado de zeros pelo byteCount (StartHTML: 0000000071).

O único conjunto de caracteres com suporte na área de transferência é Unicode em sua codificação UTF-8. Como os primeiros caracteres de UTF-8 e ASCII correspondem, a descrição é sempre ASCII, mas os bytes do contexto (começando em StartHTML) podem estar usando outros caracteres codificados em UTF-8.

O fim das linhas no cabeçalho de formato da área de transferência pode ser CR ou CR/LF ou LF.

O fragmento contém HTML puro e válido representando a área que o usuário selecionou (para copiar, por exemplo). Ele contém o texto selecionado, além das marcas de abertura e os atributos de qualquer elemento que tenha uma marca de fim dentro do texto selecionado e marcas de fim no final do fragmento para qualquer marca de início incluída. Todas as informações são necessárias para a colagem básica de um fragmento HTML.

O fragmento deve ser precedido e seguido pelos comentários HTML <!--StartFragment--> e <!--EndFragment--> (nenhum espaço é permitido entre o!--e o texto) para indicar convenientemente onde o fragmento começa e termina. Portanto, o início e o fim do fragmento são indicados pela presença desses comentários e por contagens de bytes StartFragment e endfrag na descrição. As ferramentas devem produzir essas informações. Essa redundância foi introduzida para conseguir encontrar rapidamente o início do fragmento (da contagem de bytes) e marcar a posição do fragmento diretamente na árvore HTML.

A seleção indica dentro do fragmento a área HTML exata que o usuário selecionou (para copiar, por exemplo). Isso adiciona mais informações ao fragmento indicando o texto exato selecionado, sem as marcas de abertura e marcas de fim que foram adicionadas para garantir que o fragmento seja um HTML bem formado.

A seleção é opcional, já que informações suficientes são incluídas no fragmento para a colagem básica. Se a seleção não for armazenada, StartSelection e EndSelect não serão armazenadas no cabeçalho.

O contexto é um documento HTML válido e completo. Este artigo contém o fragmento e todas as marcas adjacentes anteriores (marcas de início e de término; elas antes das marcas ao redor representam todos os nós pai do fragmento, até o nó HTML). O artigo também contém o cabeçalho completo e permite que os elementos BASE e título, por exemplo, sejam incluídos para que essas informações adicionais possam ser obtidas. Um aplicativo que copia um fragmento de HTML para a área de transferência pode optar por criar um elemento BASE para incluir no contexto se esse elemento ainda não estiver presente, de modo que as URLs parciais no fragmento possam ser resolvidas.

O contexto é opcional, pois informações suficientes são incluídas no fragmento para a colagem básica de um fragmento de HTML para ocorrer. Se o contexto não for armazenado, o fragmento somente será armazenado e o StartHTML = endhtml =-1.

## <a name="scenarios"></a>Cenários

Os cenários a seguir descrevem como o editor de HTML IE4/MSHTML trata do HTML recortar e colar; outros aplicativos podem ou não seguir esses cenários. O formato da área de transferência descrito aqui destina-se a permitir a flexibilidade de como um aplicativo opta por funcionar. (Esses cenários mostram apenas um bom HTML, ou seja, não há marcas sobrepostas.)

1.  Fragmento simples de HTML.
    -   -   Texto HTML:

            <BODY>Isso é normal. isso é <B>negrito </B>e <I> <B>negrito </B></I> é itálico</BODY>

        -   Aparece como:

            Isso é normal. isso é **negrito** e    * **negrito** é itálico   *

        -   O texto entre o \* \* é selecionado e copiado para a área de transferência:

            Isso é normal. este é **um negrito em** \* \*     * **itálico**   este * \* \* *é itálico*

        -   É isso que estará na área de transferência (Observe que é a interpretação de IE4/MSHTML):

            Versão: 0,9

            StartHTML: 71

            Endhtml: 160

            StartFragment: 130

            EndFragment: 150

            **StartSelection: 130**

            **Fim da seleção: 150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>negrito</B><I><B>este é negrito e itálico</B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   Nesse cenário, apenas a marca BODY e a marca HTML aparecem no contexto, pois ele precede o fragmento selecionado. Observe que as marcas de início e as marcas de fim são incluídas no contexto. A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.

2.  Fragmento de uma tabela em HTML.
    -   -   Texto HTML:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Item 4</TD></TR><TR><TD>Item 5</TD><TD>Item 6</TD><TD>Item 7</TD><TD>Item 8</TD></TR><TR><TH>Head2</TH><TD>Item 9</TD><TD>Item 10</TD><TD>Item 11</TD><TD>Item 12</TD></TR></TABLE></BODY>

        -   Aparece como: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Item 4</TD></TR><TR><TD>Item 5</TD><TD>Item 6</TD><TD>Item 7</TD><TD>Item 8</TD></TR><TR><TH>Head2</TH><TD>Item 9</TD><TD>Item 10</TD><TD>Item 11</TD><TD>Item 12</TD></TR></TABLE><! \[ CDATA\[\]\]>
        -   Os elementos item 6, Item7, item 10 e item 11 da tabela são selecionados como um bloco e copiados para a área de transferência.
        -   É isso que estará na área de transferência (Observe que é a interpretação de IE4/MSHTML):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Item 6 </TD> <TD> item 7 item </TD> </TR> <TR> <TD> 10 </TD> <TD> Item 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  Colando um fragmento de uma lista ordenada em texto sem formatação.
    -   -   Texto HTML:

            <BODY><OL TYPE = a><LI>Item 1<LI>Item 2<LI>Item 3<LI>Item 4<LI>Item 5<LI>Item 6</OL></BODY>

        -   Aparece como:
            1.  Item 1
            2.  Item 2
            3.  Item 3
            4.  Item 4
            5.  Item 5
            6.  Item 6
        -   O usuário seleciona e copia os itens de 3 a 5 para a área de transferência. O HTML a seguir está na área de transferência:

            <DOCTYPE... ><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Item 3 item <LI> 4 <LI> item 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.

        -   Se esse fragmento for agora colado em um documento vazio, o seguinte HTML será criado:

            <BODY><OL TYPE = a><LI>Item 3<LI>Item 4<LI>Item 5</OL></BODY>

        -   Aparecendo como:
            1.  Item 3
            2.  Item 4
            3.  Item 5

4.  Colando uma região parcialmente selecionada.
    -   -   Texto HTML:

            <P> IE4/MSHTML é um editor WYSIWYG que dá suporte a:<UL><LI>Recortar<LI>Copiar<LI>Colar</UL><P>Essa é uma excelente ferramenta!

        -   Aparece como: IE4/MSHTML é um editor WYSIWYG que dá suporte a:
            -   -   Recortar
                -   Copiar
                -   Colar

        -   O usuário seleciona "WYSIWYG" até "Cop". O HTML a seguir está na área de transferência:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, que dá suporte a**

            **<UL><LI>Recortar <LI> COP**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   O usuário seleciona "opiar" até "ótimo".

            O HTML a seguir está na área de transferência:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **opiar <LI> colar </UL> <P> este é um ótimo**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.

 

 




