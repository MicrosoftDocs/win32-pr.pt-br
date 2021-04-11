---
title: Escutando eventos da faixa de das
description: O Windows Ribbon Framework usa a infraestrutura ETW (rastreamento de eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de faixas do aplicativo.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Faixa de, eventos do Windows
- Faixa de, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294553"
---
# <a name="listening-for-ribbon-events"></a>Escutando eventos da faixa de das

O Windows Ribbon Framework usa a infraestrutura [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de faixas do aplicativo.

## <a name="introduction"></a>Introdução

O mecanismo de eventos da estrutura da faixa de faixas foi projetado de modo que a estrutura relate eventos da interface do usuário da faixa de da forma para que você possa monitorar a atividade do usuário, aprender seus padrões de interação e avaliar tendências de uso. Essas informações podem ser usadas para refinar a experiência do usuário para iterações futuras do seu aplicativo da faixa de faixas.

O uso dos eventos da estrutura da faixa de opções envolve o seguinte:

1.  O aplicativo da faixa de faixas deve registrar um ouvinte [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para receber notificações de eventos da faixa de faixas.
2.  A estrutura da faixa de chamadas dispara retornos de chamada de evento da interface do usuário em tempo de execução, se o aplicativo tiver registrado um ouvinte [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) .

## <a name="supported-events"></a>Eventos com suporte

Os eventos expostos aos aplicativos da faixa de opções são descritos na tabela a seguir. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Relatório de eventos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Guia ativada</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Guia contextual ativada</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Menu do aplicativo aberto</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Menu do aplicativo fechado</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Menu (regular ou galeria) aberto</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo de evento<br/>
<blockquote>
[!Note]<br />
Os eventos do menu QAT não são expostos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menu (regular ou galeria) fechado</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo de evento<br/>
<blockquote>
[!Note]<br />
Os eventos do menu QAT não são expostos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Comando</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo de evento<br/> Um dos seguintes locais de evento:
<ul>
<li>3D</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> ID do comando pai<br/> Nome do comando pai<br/> Um dos seguintes métodos Invoke:
<ul>
<li>Selecione</li>
<li>KEYTIP</li>
<li>TECLADO</li>
<li>Tom</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
As galerias de itens e as caixas de combinação incluem o índice de item selecionado, mas não incluem valores de cadeia de caracteres e inteiros. Os eninteriors não incluem o valor inteiro.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Faixa de faixas minimizada</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Faixa de faixas expandida (botão de expansão clicado ou toque fixado)</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Modo de aplicativo alternado</td>
<td>Verbo de evento<br/> ID do modo (valor definido por meio de <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>modos</strong></a>)<br/>
<blockquote>
[!Note]<br />
O aplicativo é responsável por desempacotar esse inteiro para determinar quais modos foram definidos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Dica de ferramenta exibida</td>
<td>Verbo de evento<br/> ID do comando pai<br/> Nome do comando pai<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guias de desenvolvedor do Windows Ribbon Framework](windowsribbon-guides-entry.md)
</dt> <dt>

[Declarando comandos e controles com marcação de faixa de medida](./windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de das](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

