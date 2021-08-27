---
description: Introdução (guia Windows 7 e Windows Server 2008 R2 Application Quality)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introdução (guia Windows 7 e Windows Server 2008 R2 Application Quality)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb61f41644f74e22f8e4117854db90cc1bea025b3ff5399819eaa580eee39f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994916"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introdução (guia Windows 7 e Windows Server 2008 R2 Application Quality)

Em todo o mundo, muitas empresas estão adotando Windows 7 devido a seus recursos e habilidades empresariais. Os departamentos de TI também estão alterando a maneira como abordam suas necessidades de plataforma de longo prazo para dar suporte a uma área de trabalho moderna. O Windows 7 ajuda a reduzir o custo total de propriedade, ajudando os usuários a permanecerem produtivos em qualquer lugar, aprimoram a segurança e o controle e simplificam o gerenciamento da área de trabalho em toda a organização. Windows 7 também inclui um navegador moderno baseado em padrões, Windows Internet Explorer 8, que fornece segurança aprimorada e funcionalidades de navegação aprimoradas. Essas duas plataformas aumentam a eficiência de TI e aprimoram a agilidade e a segurança de uma organização.

No entanto, migrar para um novo sistema operacional cria desafios exclusivos, principalmente com a necessidade de dar suporte a aplicativos Web herdáveis. As empresas podem ter aplicativos que foram construídos para versões anteriores do Windows Internet Explorer, como Windows Internet Explorer 7 ou Microsoft Internet Explorer 6. Esses aplicativos Web podem encontrar problemas de compatibilidade com Internet Explorer 8. Além disso, Internet Explorer 6 não é executado na Windows 7 e Windows não dá suporte à execução de duas versões do Internet Explorer simultaneamente. Para obter mais informações, consulte o artigo Base de Dados de Conhecimento Microsoft " Executando várias versões do[Internet Explorer no sistema](https://support.microsoft.com/kb/2020599)operacional único não tem suporte".

Muitas empresas ainda usam Internet Explorer aplicativos Web baseados em 6 que foram construídos e personalizados na última década. As empresas que planejam implantar o Windows 7 precisam ter uma estratégia abrangente e um plano de execução em ação para migrar aplicativos Web herdado para Internet Explorer 8. Este documento fornece uma visão geral detalhada dos Internet Explorer 8 problemas de compatibilidade, discute como migrar aplicativos Web e apresenta ferramentas e processos relacionados.

A Internet Explorer 8 se concentrou em três temas principais:

-   Forneça interoperabilidade do mundo real com outros navegadores e compatibilidade para sites existentes.
-   Tornar o desenvolvimento na Web mais rápido e mais fácil usando as ferramentas internas para desenvolvedores.
-   Habilita experiências que vão além da página, por meio de novos recursos do navegador que conectam os usuários a serviços Web inovadores.

Além de avanços significativos no suporte a padrões, o Internet Explorer 8 contém investimentos adicionais de plataforma para desenvolvedores. Internet Explorer 8 melhora o desempenho em muitos subsistemas do Internet Explorer, como o analisador HTML, o processamento de regra css (folha de estilos em cascata), a manipulação de árvore de marcação, o analisador JavaScript, o runtime do coletor de lixo e o gerenciamento de memória. Os investimentos adicionais para desenvolvedores incluem:

-   CSS 2.1: você pode escrever suas páginas uma vez e fazer com que elas possam ser renderizações mais facilmente em diferentes navegadores, pois o Internet Explorer 8 dá suporte total à especificação CSS 2.1.
-   Modelo de Objeto do Documento (DOM) e HTML 4.01: o Internet Explorer 8 fornece melhorias adicionais do HTML 4.01 e conformidade completa do CSS 2.1. Internet Explorer 8 também corrige muitas inconsistências entre navegadores. Por exemplo, a implementação de atributo get/set/remove agora é interoperável com outros navegadores e o desempenho é aprimorado em padrões de design assíncronos de JavaScript e XML (AJAX).
-   Padrões emergentes: o Internet Explorer 8 incorpora padrões futuros, como o padrão HTML5 Draft DOM Armazenamento do W3C, a API de Seletores do Grupo de Trabalho de Aplicativos Web e a sintaxe endossada do ECMAScript 3.1.
-   Novos recursos de navegação para aplicativos AJAX: você pode atualizar a pilha de navegação de voltar e encaminhar do navegador e a Barra de Endereços de aplicativos AJAX para que esses recursos do navegador funcionem corretamente em seu aplicativo.
-   Acid2: Internet Explorer 8 renderiza o teste do navegador Acid2 corretamente.
-   Compatibilidade: Internet Explorer 8 inclui um mecanismo de layout mais compatível com padrões que permite criar um site baseado em padrões para vários navegadores. Para migrar seus sites com mais facilidade para o novo mecanismo de layout em conformidade com padrões, o Internet Explorer 8 permite que você use o mecanismo de layout do Internet Explorer 7 inserindo um **metadado** simples em seu código ou adicionando um único cabeçalho HTTP em seus servidores.
-   Ferramentas para Desenvolvedores: Ferramentas para Desenvolvedores no Internet Explorer (que você acessa pressionando a tecla F12) permite depurar rapidamente o código HTML, CSS e JavaScript em um ambiente visual. Essas ferramentas são incluídas diretamente no Internet Explorer 8 com funcionalidade expandida, incluindo a opção ann para escolher qual aplicativo usar quando você estiver exibindo a origem de uma página da Web. Você pode identificar e resolver problemas rapidamente devido ao insight profundo que a ferramenta fornece ao DOM.
-   Para obter mais informações sobre os recursos novos e aprimorados do Internet Explorer 8, consulte Novidades no [Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) no Biblioteca MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



