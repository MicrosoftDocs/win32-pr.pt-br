---
title: Modelo de objeto de texto
description: Esta seção contém informações sobre os elementos de programação usados com o modelo de objeto de texto (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103824037"
---
# <a name="text-object-model"></a>Modelo de objeto de texto

Esta seção contém informações sobre os elementos de programação usados com o modelo de objeto de texto (TOM).

José define um conjunto substancial de interfaces de manipulação de texto. Soluções de texto como o Microsoft Word e os controles rich edit dão suporte ao conjunto de recursos TOM. José foi bastante influenciado pelo WordBasic (a linguagem de programação usada para o Word) e é fácil de usar do Microsoft Visual Basic for Applications (VBA). Essa compatibilidade tem várias vantagens:

-   O código pode migrar razoavelmente facilmente de uma solução para outra.
-   Uma linguagem pode ser usada para compartilhar informações de texto entre diferentes mecanismos de texto.
-   Ele reduz a necessidade de documentação e código em comparação com as interfaces COM (Component Object Model de baixo nível) e VBA separadas.

No entanto, isso pode ser menos eficiente para fins de C/C++ do que o uso de interfaces COM de nível inferior mais gerais.

José é um conjunto simples de interfaces a serem implementadas para suas soluções de texto primários, palavras e controles de edição avançados. No entanto, para aplicativos que colocam ênfase mínima no texto, é melhor fornecer interfaces de TOM transferindo o texto para um controle de edição que dá suporte a TOM. Como os controles de edição avançados são fornecidos com os sistemas operacionais da Microsoft, eles são o meio padrão de obter a funcionalidade de TOM.

### <a name="overviews"></a>Visões gerais



| Tópico                                                          | Sumário                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o modelo de objeto de texto](about-text-object-model.md)         | O objeto TOM (modelo de objeto de texto) de nível superior é definido pela interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , que tem métodos para criar e recuperar objetos inferiores na hierarquia de objetos.<br/> |
| [Usando o modelo de objeto de texto](using-the-text-object-model.md) | Os exemplos de código neste documento mostram vários aspectos do uso do TOM (modelo de objeto de texto).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Interfaces



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td>A interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> é a interface de alto nível de Tom, que recupera a seleção ativa e os objetos de intervalo para qualquer história no documento, esteja ela ativa ou não. Ele permite que o aplicativo:
<ul>
<li>Abra e salve documentos.</li>
<li>Controlar o comportamento de desfazer e a atualização de tela.</li>
<li>Localize um intervalo de uma posição de tela.</li>
<li>Obtenha um enumerador de história do <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> .</li>
</ul>
<br/> <strong>Quando implementar</strong><br/> Normalmente, os aplicativos não implementam a interface <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> . Soluções de texto da Microsoft, como controles de edição avançados, implementam <strong>ITextDocument</strong> como parte de sua implementação de Tom. <br/> <strong>Quando usar</strong><br/> Os aplicativos podem recuperar um ponteiro <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> de um controle de edição rico. Para fazer isso, envie uma mensagem de <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> para recuperar um objeto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> de um controle de edição rico. Em seguida, chame o método <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> do objeto para recuperar um ponteiro <strong>ITextDocument</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></td>
<td>José os atributos de intervalo de texto avançados são acessados por meio de um par de interfaces duplas, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></td>
<td>José os atributos de intervalo de texto avançados são acessados por meio de um par de interfaces duplas, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></td>
<td>Os objetos <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> são ferramentas poderosas de edição e vinculação de dados que permitem que um programa selecione texto em uma história e, em seguida, examine ou altere esse texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></td>
<td>Uma seleção de texto é um intervalo de texto com realce de seleção.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></td>
<td>A finalidade da interface <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> é enumerar as histórias em um <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

