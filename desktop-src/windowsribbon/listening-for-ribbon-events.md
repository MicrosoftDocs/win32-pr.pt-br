---
title: Escutando eventos da faixa de opções
description: A Windows faixa de opções usa a infraestrutura ETW (Rastreamento de Eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de opções do aplicativo.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Faixa de opções, eventos
- Faixa de opções, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9519553a40cd613085949d4650c2689e817f387e47e9ab4380b629464e90d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202966"
---
# <a name="listening-for-ribbon-events"></a>Escutando eventos da faixa de opções

A Windows faixa de opções usa a infraestrutura [ETW (Rastreamento](../etw/event-tracing-portal.md) de Eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de opções do aplicativo.

## <a name="introduction"></a>Introdução

O mecanismo de evento da estrutura ribbon foi projetado de modo que a estrutura relata eventos de interface do usuário da faixa de opções para o aplicativo para que você possa monitorar a atividade do usuário, aprender seus padrões de interação e avaliar as tendências de uso. Essas informações podem ser usadas para refinar a experiência do usuário para ierções futuras de seu aplicativo de faixa de opções.

O uso dos eventos da estrutura da Faixa de Opções envolve o seguinte:

1.  O aplicativo de faixa de opções deve registrar um ouvinte [ETW (Rastreamento de Windows)](../etw/event-tracing-portal.md) para receber notificações de evento da faixa de opções da estrutura ribbon.
2.  A estrutura da Faixa de Opções dispara retornos de chamada de evento da interface do usuário da faixa de opções em tempo de executar, se o aplicativo tiver registrado um ouvinte [etw (Rastreamento](../etw/event-tracing-portal.md) de Eventos para Windows).

## <a name="supported-events"></a>Eventos com suporte

Os eventos expostos aos aplicativos de faixa de opções são descritos na tabela a seguir. 

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
<td>ID do comando<br/> Nome de comando<br/> Verbo do evento<br/></td>
</tr>
<tr class="even">
<td>Guia contextual ativada</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo do evento<br/></td>
</tr>
<tr class="odd">
<td>Menu do Aplicativo aberto</td>
<td>Verbo do evento<br/></td>
</tr>
<tr class="even">
<td>Menu do Aplicativo fechado</td>
<td>Verbo do evento<br/></td>
</tr>
<tr class="odd">
<td>Menu (regular ou galeria) aberto</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo do evento<br/>
<blockquote>
[!Note]<br />
Eventos de menu QAT não são expostos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menu (regular ou galeria) fechado</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo do evento<br/>
<blockquote>
[!Note]<br />
Eventos de menu QAT não são expostos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Comando</td>
<td>ID do comando<br/> Nome de comando<br/> Verbo do evento<br/> Um dos seguintes locais de evento:
<ul>
<li>Fita</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> ID do comando pai<br/> Nome do comando pai<br/> Um dos seguintes métodos de invocação:
<ul>
<li>Clique</li>
<li>Keytip</li>
<li>Teclado</li>
<li>Toque</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Galerias de itens e caixas de combinação incluem o índice de item selecionado, mas não incluem valores de cadeia de caracteres e inteiros. Os giradores não incluem o valor inteiro.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Faixa de opções minimizada</td>
<td>Verbo do evento<br/></td>
</tr>
<tr class="odd">
<td>Faixa de opções expandida (botão expandir clicado ou toque fixado)</td>
<td>Verbo do evento<br/></td>
</tr>
<tr class="even">
<td>Modo de aplicativo comutado</td>
<td>Verbo do evento<br/> ID do modo (valor definido por <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>meio de SetModes</strong></a>)<br/>
<blockquote>
[!Note]<br />
O aplicativo é responsável por desempacotar esse inteiro para determinar quais modos foram definidos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Dica de ferramenta exibida</td>
<td>Verbo do evento<br/> ID do comando pai<br/> Nome do comando pai<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Guias do desenvolvedor da Estrutura de Faixa de Opções](windowsribbon-guides-entry.md)
</dt> <dt>

[Declarando comandos e controles com marcação de faixa de opções](./windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de opções](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de opções](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

