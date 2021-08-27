---
title: Formato da área de transferência HTML
description: Esta seção discute o formato da Área de Transferência HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Interface do Usuário, área de transferência
- área de transferência, reduzindo dados
- área de transferência, copiando dados
- área de transferência, colar dados
- área de transferência, formatos
- área de transferência, formato HTML
- área de transferência, reduzindo o texto HTML
- área de transferência, colar texto HTML
- CF_HTML da área de transferência
- área de transferência, CF_HTML formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d73b5101d26fc55002d55e0c15144646b80445
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884989"
---
# <a name="html-clipboard-format"></a>Formato da área de transferência HTML

Os requisitos para transferir texto HTML por meio da área de transferência diferem dependendo do cenário. Este artigo se preocupa com o corte e a colar fragmentos de um documento HTML. Pode haver requisitos para transferir documentos HTML inteiros por meio da área de transferência; no entanto, este artigo é orientado por um requisito para transferir fragmentos de texto HTML selecionado. Assim, um método que exigia que todo o documento HTML fosse copiado para a área de transferência é visto como muito pesado.

O formato da área de transferência HTML do CF permite que um fragmento de texto HTML bruto e seu contexto sejam armazenados na área de \_ transferência como ASCII. Isso permite que o contexto do fragmento HTML, que consiste em todas as marcas ao redor anteriores, seja examinado por um aplicativo para que as marcas ao redor do fragmento HTML possam ser notadas com seus atributos. Embora seja responsabilidade dos aplicativos decidir como interpretar esses fragmentos, algumas diretrizes básicas são incluídas aqui com base em implementações de IE4/MSHTML.

O nome oficial da área de transferência (a cadeia de caracteres usada por RegisterClipboardFormat) é Formato HTML.

-   [Descrição](#description)
-   [Cenários](#scenarios)

## <a name="description"></a>Description

CF HTML é totalmente o formato de texto (para ser, entre outras coisas, no idioma HTML e usa UTF-8) e inclui um , um opcional e, dentro do \_ `description` `context` contexto, o `fragment` .

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



A descrição inclui o número de versão e deslocamentos da área de transferência, indicando onde o contexto e o fragmento começam e terminam. A descrição é uma lista de palavras-chave de texto ASCII (min/major não é significativo) seguidas por uma cadeia de caracteres e separadas por dois-pontos (:).

**Versão:** número de versão vv da área de transferência. A versão inicial é 0.9.

**StartHTML:** bytecount do início da área de transferência até o início do contexto ou -1 se nenhum contexto.

**EndHTML:** contagem de byte do início da área de transferência até o final do contexto ou -1 se nenhum contexto.

**StartFragment**: bytecount do início da área de transferência para o início do fragmento.

**EndFragment**: bytecount do início da área de transferência até o final do fragmento.

**StartSelection**: bytecount do início da área de transferência até o início da seleção.

**EndSelection**: bytecount do início da área de transferência até o final da seleção.

As palavras-chave StartSelection e EndSelection são opcionais e devem ser omitidas se você não quiser que o aplicativo gere essas informações.

Outras informações desse tipo podem ser adicionadas aqui mais tarde, pois o HTML começa no StartHTMLoffset. Por exemplo, vários pares de StartFragment/EndFragment podem ser adicionados posteriormente para dar suporte à seleção não contígua de fragmentos.

Para a conveniência dos programas que geram as conta de byte, as contagems de byte podem ser deixadas em zeros. Por exemplo, programas que geram as contas de byte podem afetar arbitrariamente dez (10) zeros para cada palavra-chave (StartHTML: 0000000000) e, em seguida, quando a contagem de bytecount StartHTML exata é conhecida (digamos, 71), o programa pode substituir o número apropriado de zeros pela contagem de byte (StartHTML: 0000000071).

O único conjunto de caracteres com suporte pela área de transferência é Unicode em sua codificação UTF-8. Como os primeiros caracteres de UTF-8 e ASCII são correspondam, a descrição é sempre ASCII, mas os bytes do contexto (começando em StartHTML) podem estar usando qualquer outro caractere codificado em UTF-8.

O fim das linhas no header de formato da área de transferência pode ser CR ou CR/LF ou LF.

O fragmento contém HTML puro e válido que representa a área selecionada pelo usuário (para Copiar, por exemplo). Isso contém o texto selecionado mais as marcas de abertura e os atributos de qualquer elemento que tenha uma marca de término dentro do texto selecionado e marcas de término no final do fragmento para qualquer marca de início incluída. Essas são todas as informações necessárias para a colar básica de um fragmento HTML.

O fragmento deve ser precedido e seguido pelos comentários HTML <!--StartFragment--> e <!--EndFragment--> (nenhum espaço permitido entre o !-- e o texto) para indicar convenientemente onde o fragmento começa e termina. Portanto, o início e o final do fragmento são indicados pela presença desses comentários e pelas contagens de byte StartFragment e EndFragment na descrição. Espera-se que as ferramentas produzam essas informações. Essa redundância foi introduzida para ser capaz de encontrar rapidamente o início do fragmento (da contagem de byte) e marcar a posição do fragmento diretamente na árvore HTML.

A seleção indica dentro do fragmento a área HTML exata que o usuário selecionou (para Copiar, por exemplo). Isso adiciona mais informações ao fragmento indicando o texto selecionado exato, sem as marcas de abertura e as marcas de extremidade que foram adicionadas para garantir que o fragmento seja HTML bem formado.

A seleção é opcional, pois informações suficientes são incluídas no fragmento para colar básico. Se a seleção não estiver armazenada, StartSelection e EndSelection não serão armazenados no header.

O contexto é um documento HTML válido e completo. Este artigo contém o fragmento e todas as marcas ao redor anteriores (marcas de início e término; essas marcas adjacentes anteriores representam todos os nós pai do fragmento, até o nó HTML). O artigo também contém o HEAD completo e permite que os elementos BASE e TITLE, por exemplo, sejam incluídos para que essas informações adicionais possam ser obtidas. Um aplicativo que copia um fragmento de HTML para a área de transferência pode optar por criar um elemento BASE para incluir no contexto se esse elemento ainda não estiver presente para que as URLs parciais no fragmento possam ser resolvidas.

O contexto é opcional, pois informações suficientes são incluídas no fragmento para que a pastagem básica de um fragmento HTML seja realizada. Se o contexto não for armazenado, o fragmento será armazenado somente e StartHTML=EndHTML=-1.

## <a name="scenarios"></a>Cenários

Os cenários a seguir descrevem como o editor HTML IE4/MSHTML lida com recortar e colar HTML; outros aplicativos podem ou não seguir esses cenários. O formato da área de transferência descrito aqui destina-se a permitir a flexibilidade de como um aplicativo opta por funcionar. (Esses cenários mostram apenas um HTML bom, ou seja, sem marcas sobrepostas.)

1.  Fragmento simples de HTML.
    -   -   Texto HTML:

            &lt;BODY &gt; Isso é normal Este é <B>negrito </B> <I> <B>Este é itálico em negrito </B>Este é itálico </I> &lt; /BODY&gt;

        -   Aparece como:

            Isso é normal **Este é negrito**  **_Este é um itálico em negrito_*  Este é itálico*

        -   O texto entre o \* \* é selecionado e copiado para a área de transferência:

            Isso é normal **Este é** \* \* **negrito****_Este é um itálico em negrito_** \* \* *Este é itálico*   

        -   Isso é o que estará na área de transferência (observe que esta é a interpretação de IE4/MSHTML):

            Versão:0.9

            StartHTML:71

            EndHTML:160

            StartFragment:130

            EndFragment:150

            **StartSelection:130**

            **EndSelection:150**

            <!DOCTYPE ...>

            &lt;CORPO&gt;

            <!-- StartFragment -->>

            **<B>negrito</B><I><B>Este é um itálico em negrito</B></I>**

            <!-- EndFragment -->

            &lt;/BODY&gt;

            &lt;/HTML&gt;

        -   Nesse cenário, somente a marca BODY e a marca HTML aparecem no contexto à medida que precedem o fragmento selecionado. Observe que marcas de início e marcas de término estão incluídas no contexto. A seleção, conforme delimitada por StartSelection e EndSelection, é mostrada em negrito.

2.  Fragmento de uma tabela em HTML.
    -   -   Texto HTML:

            &lt;CORPO&gt;<TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Item 4</TD></TR><TR><TD>Item 5</TD><TD>Item 6</TD><TD>Item 7</TD><TD>Item 8</TD></TR><TR><TH>Head2</TH><TD>Item 9</TD><TD>Item 10</TD><TD>Item 11</TD><TD>Item 12</TD></TR></TABLE>&lt;/BODY&gt;

        -   Aparece como: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Item 2</TD><TD>Item 3</TD><TD>Item 4</TD></TR><TR><TD>Item 5</TD><TD>Item 6</TD><TD>Item 7</TD><TD>Item 8</TD></TR><TR><TH>Head2</TH><TD>Item 9</TD><TD>Item 10</TD><TD>Item 11</TD><TD>Item 12</TD></TR></TABLE><! \[ CDATA\[\]\]>
        -   Os elementos item 6, Item7, item 10 e item 11 da tabela são selecionados como um bloco e copiados para a área de transferência.
        -   É isso que estará na área de transferência (Observe que é a interpretação de IE4/MSHTML):

            <!DOCTYPE ...>

            &lt;&gt; &lt; corpo HTML&gt;<TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Item 6 </TD> <TD> item 7 item </TD> </TR> <TR> <TD> 10 </TD> <TD> Item 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            &lt;/BODY &gt; &lt; /HTML &gt; a seleção, como delimitada por StartSelection e endseleções, é mostrada em negrito.

3.  Colando um fragmento de uma lista ordenada em texto sem formatação.
    -   -   Texto HTML:

            &lt;CONTEÚDO&gt;<OL TYPE = a><LI>Item 1<LI>Item 2<LI>Item 3<LI>Item 4<LI>Item 5<LI>Item 6</OL>&lt;/BODY&gt;

        -   Aparece como:
            1.  Item 1
            2.  Item 2
            3.  Item 3
            4.  Item 4
            5.  Item 5
            6.  Item 6
        -   O usuário seleciona e copia os itens de 3 a 5 para a área de transferência. O HTML a seguir está na área de transferência:

            <DOCTYPE... >&lt; &gt; &lt; corpo HTML&gt;<OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Item 3 item <LI> 4 <LI> item 5**

            <!-- EndFragment-->

            </OL>&lt;/BODY&gt;&lt;/HTML&gt;

            A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.

        -   Se esse fragmento for agora colado em um documento vazio, o seguinte HTML será criado:

            &lt;CONTEÚDO&gt;<OL TYPE = a><LI>Item 3<LI>Item 4<LI>Item 5</OL>&lt;/BODY&gt;

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

            <DOCTYPE... >&lt; &gt; &lt; corpo HTML&gt;

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, que dá suporte a**

            **<UL><LI>Recortar <LI> COP**

            </UL>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML &gt; a seleção, como delimitada por StartSelection e endseleções, é mostrada em negrito.

     
    -   -   O usuário seleciona "opiar" até "ótimo".

            O HTML a seguir está na área de transferência:

            <DOCTYPE... >&lt; &gt; &lt; corpo HTML&gt;

            <!-- StartFragment-->

            <UL><LI>

            **opiar <LI> colar </UL> <P> este é um ótimo**

            </P>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML&gt;

            A seleção, como delimitada por StartSelection e endselectation, é mostrada em negrito.

 

 




