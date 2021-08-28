---
title: Escutando eventos da faixa de opções
description: A Windows faixa de opções usa a infraestrutura ETW (Rastreamento de Eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de opções do aplicativo.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Faixa de opções, eventos
- Faixa de opções, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf28052aa741437a7f96f90ddb1b4a773ae4c4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473032"
---
# <a name="listening-for-ribbon-events"></a>Escutando eventos da faixa de opções

A Windows faixa de opções usa a infraestrutura [ETW (Rastreamento](../etw/event-tracing-portal.md) de Eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de opções do aplicativo.

## <a name="introduction"></a>Introdução

O mecanismo de evento da estrutura ribbon foi projetado de modo que a estrutura relata eventos de interface do usuário da faixa de opções para o aplicativo para que você possa monitorar a atividade do usuário, aprender seus padrões de interação e avaliar as tendências de uso. Essas informações podem ser usadas para refinar a experiência do usuário para ierções futuras de seu aplicativo de faixa de opções.

O uso dos eventos da estrutura da Faixa de Opções envolve o seguinte:

1.  O aplicativo de faixa de opções deve registrar um [ouvinte ETW (Rastreamento de Windows)](../etw/event-tracing-portal.md) para receber notificações de eventos da faixa de opções da estrutura da Faixa de Opções.
2.  A estrutura da Faixa de Opções dispara retornos de chamada de evento da interface do usuário da faixa de opções em tempo de executar, se o aplicativo tiver registrado um ouvinte [etw (Rastreamento](../etw/event-tracing-portal.md) de Eventos para Windows).

## <a name="supported-events"></a>Eventos com suporte

Os eventos expostos aos aplicativos de faixa de opções são descritos na tabela a seguir. 


| Evento | Relatório de eventos | 
|-------|--------------|
| Guia ativada | ID do comando<br /> Nome de comando<br /> Verbo do evento<br /> | 
| Guia contextual ativada | ID do comando<br /> Nome de comando<br /> Verbo do evento<br /> | 
| Menu do Aplicativo aberto | Verbo do evento<br /> | 
| Menu do Aplicativo fechado | Verbo do evento<br /> | 
| Menu (regular ou galeria) aberto | ID do comando<br /> Nome de comando<br /> Verbo do evento<br /><blockquote>[!Note]<br />Eventos de menu QAT não são expostos.</blockquote><br /> | 
| Menu (regular ou galeria) fechado | ID do comando<br /> Nome de comando<br /> Verbo do evento<br /><blockquote>[!Note]<br />Eventos de menu QAT não são expostos.</blockquote><br /> | 
| Comando | ID do comando<br /> Nome de comando<br /> Verbo do evento<br /> Um dos seguintes locais de evento:<ul><li>FITA</li><li>QUICKACCESSTOOLBAR</li><li>APPLICATIONMENU</li><li>CONTEXTPOPUP</li></ul><br /> ID do comando pai<br /> Nome do comando pai<br /> Um dos seguintes métodos de invocação:<ul><li>CLIQUE</li><li>KEYTIP</li><li>TECLADO</li><li>TOQUE</li></ul><br /><blockquote>[!Note]<br />Galerias de itens e caixas de combinação incluem o índice de item selecionado, mas não incluem valores de cadeia de caracteres e inteiros. Os giradores não incluem o valor inteiro.</blockquote><br /> | 
| Faixa de opções minimizada | Verbo do evento<br /> | 
| Faixa de opções expandida (botão expandir clicado ou toque fixado) | Verbo do evento<br /> | 
| Modo de aplicativo comutado | Verbo do evento<br /> ID do modo (valor definido por <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>meio de SetModes</strong></a>)<br /><blockquote>[!Note]<br />O aplicativo é responsável por desempacotar esse inteiro para determinar quais modos foram definidos.</blockquote><br /> | 
| Dica de ferramenta exibida | Verbo do evento<br /> ID do comando pai<br /> Nome do comando pai<br /> | 




 

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

