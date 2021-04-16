---
description: .
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introdução (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d491802735ddf1ef75a7a183cd49afea2cc657b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750152"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introdução (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

Em todo o mundo, muitas empresas estão adotando o Windows 7 devido a seus recursos e capacidades empresariais. Os departamentos de ti também estão mudando como eles abordam a plataforma de longo prazo que precisam dar suporte a uma área de trabalho moderna. O sistema operacional Windows 7 ajuda a reduzir o custo total de propriedade, ajudando os usuários a se manterem produtivos em qualquer lugar, aprimorar a segurança e o controle e simplificar o gerenciamento de desktops em toda a organização. O Windows 7 também inclui um navegador moderno baseado em padrões, o Windows Internet Explorer 8, que fornece segurança aprimorada e recursos de navegação aprimorados. Essas duas plataformas aumentam a eficiência de ti e melhoram a agilidade e a segurança de uma organização.

No entanto, migrar para um novo sistema operacional cria desafios exclusivos, principalmente com a necessidade de dar suporte a aplicativos Web herdados. As empresas podem ter aplicativos criados para versões anteriores do Windows Internet Explorer, como o Windows Internet Explorer 7 ou o Microsoft Internet Explorer 6. Esses aplicativos Web podem encontrar problemas de compatibilidade com o Internet Explorer 8. Além disso, o Internet Explorer 6 não é executado nativamente no Windows 7 e o Windows não oferece suporte à execução de duas versões do Internet Explorer simultaneamente. Para obter mais informações, consulte o artigo da base de dados de conhecimento Microsoft, "[não há suporte para executar várias versões do Internet Explorer em um único sistema operacional](https://support.microsoft.com/kb/2020599)."

Muitas empresas ainda usam aplicativos Web baseados no Internet Explorer 6 que foram criados e personalizados na última década. As empresas que planejam implantar o Windows 7 precisam ter uma estratégia abrangente e um plano de execução em vigor para migrar aplicativos Web herdados para o Internet Explorer 8. Este documento fornece uma visão geral detalhada dos problemas de compatibilidade do Internet Explorer 8, discute como migrar aplicativos Web e apresenta processos e ferramentas relacionadas.

A versão do Internet Explorer 8 concentra-se em três temas principais:

-   Forneça interoperabilidade do mundo real com outros navegadores e compatibilidade para sites existentes.
-   Torne o desenvolvimento para a Web mais rápido e fácil usando as ferramentas de desenvolvedor internas.
-   Habilite as experiências que chegam além da página, por meio de novos recursos de navegador que conectam os usuários aos serviços Web inovadores.

Além de avanços significativos no suporte a padrões, o Internet Explorer 8 contém investimentos de plataforma adicionais para os desenvolvedores. O Internet Explorer 8 melhora o desempenho em muitos subsistemas do Internet Explorer, como o analisador HTML, o processamento de regras CSS (folha de estilos em cascata), a manipulação de árvore de marcação, o analisador de JavaScript, o tempo de execução do coletor de lixo e o gerenciamento de memória. Os investimentos adicionais do desenvolvedor incluem:

-   CSS 2,1: você pode escrever suas páginas uma vez e fazer com que elas sejam renderizadas de forma mais fácil em diferentes navegadores, pois o Internet Explorer 8 dá suporte total à especificação CSS 2,1.
-   Melhorias de Modelo de Objeto do Documento (DOM) e HTML 4, 1: o Internet Explorer 8 fornece aprimoramentos HTML 4, 1 adicionais e conformidade total com o CSS 2,1. O Internet Explorer 8 também corrige muitas inconsistências entre navegadores. Por exemplo, a implementação de atributo Get/Set/remove agora é interoperável com outros navegadores, e o desempenho é melhorado em padrões de design JavaScript e XML (AJAX) assíncronos.
-   Padrões emergentes: o Internet Explorer 8 incorpora padrões futuros, como o padrão de armazenamento DOM de rascunho do W3C's HTML5, a API de seletores do grupo de trabalho de aplicativos Web e a sintaxe endossada ECMAScript 3,1.
-   Novos recursos de navegação para aplicativos AJAX: você pode atualizar a pilha de navegação para frente e para trás e a barra de endereços de um aplicativo AJAX para que os recursos do navegador funcionem corretamente em seu aplicativos.
-   Acid2: o Internet Explorer 8 renderiza o teste do navegador Acid2 corretamente.
-   Compatibilidade: o Internet Explorer 8 inclui um mecanismo de layout compatível com mais padrões que permite criar um site baseado em padrões para vários navegadores. Para migrar seus sites mais facilmente para o novo mecanismo de layout em conformidade com os padrões, o Internet Explorer 8 permite que você use o mecanismo de layout do Internet Explorer 7 inserindo um simples elemento **meta** em seu código ou adicionando um único cabeçalho HTTP em seus servidores.
-   Ferramentas para Desenvolvedores: Ferramentas para Desenvolvedores no Internet Explorer (que você acessa pressionando a tecla F12) permite que você depure rapidamente código HTML, CSS e JavaScript em um ambiente visual. Essas ferramentas estão incluídas diretamente no Internet Explorer 8 com funcionalidade expandida, incluindo a opção Ana para escolher qual aplicativo usar ao exibir a origem de uma página da Web. Você pode identificar e resolver problemas rapidamente devido à profunda percepção que a ferramenta fornece ao DOM.
-   Para obter mais informações sobre os recursos novos e aprimorados do Internet Explorer 8, consulte [o que há de novo no Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) na biblioteca do MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



