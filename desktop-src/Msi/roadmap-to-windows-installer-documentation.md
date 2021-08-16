---
description: esta documentação é a principal fonte de material de referência para Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: roteiro para Windows Installer documentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625906"
---
# <a name="roadmap-to-windows-installer-documentation"></a>roteiro para Windows Installer documentação

esta documentação é a principal fonte de material de referência para Windows Installer. Ele fornece informações sobre pacotes de instalação e o serviço do instalador. Ele também fornece descrições completas da API (interface de programação de aplicativo) e dos elementos do banco de dados do instalador. esta documentação também contém uma discussão sobre exemplos básicos de pacotes de instalação e atualização em [Windows Installer exemplos](windows-installer-examples.md).

o [guia baseado em função para Windows Installer documentação](role-based-guide-to-windows-installer-documentation.md) é uma alternativa fornecida como um guia para os leitores que preferem ver links para tópicos organizados por funções profissionais e cenários comuns de tarefas.

para obter informações sobre Windows Installer grupos de notícias, consulte também o tópico: [outras fontes de Windows Installer informações](other-sources-of-windows-installer-information.md).

para obter uma lista de dicas sobre como usar o Windows Installer, consulte [Windows Installer práticas recomendadas](windows-installer-best-practices.md).

A lista a seguir descreve cada seção da documentação do instalador.

-   [sobre o Windows Installer](about-windows-installer.md) fornece uma visão geral dos recursos e benefícios do instalador, como anúncio, instalação sob demanda, resiliência, personalização e gerenciamento de componentes. Esta seção apresenta os conceitos de componentes e recursos do instalador, que são essenciais para entender como o instalador organiza uma instalação. Ele também aborda vários assuntos de alto nível sobre a instalação, como política do sistema, regras de controle de versão de arquivo e reversão da instalação.
-   o [uso de Windows Installer](using-windows-installer.md) discute uma variedade de tópicos, como um método padrão para organizar um aplicativo em componentes que o instalador pode instalar ou remover do computador de um usuário; Como baixar um pacote de instalação do World Wide Web; e usando imagens de origem compactadas.
-   as informações nas seções [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md) podem ser usadas para identificar novos recursos que não têm suporte nas versões anteriores do Windows Installer.
-   [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) descreve como as assinaturas digitais podem ser usadas com pacotes, transformações, patches, módulos de mesclagem e arquivos de gabinete externo.
-   [assemblies](assemblies.md) explica como usar Windows Installer para instalar e gerenciar o tempo de execução de linguagem comum e Assemblies do Win32.
-   A [interface do usuário](user-interface.md) fornece informações sobre os recursos da interface do usuário do instalador. Embora o instalador não forneça uma interface do usuário, um autor de pacote pode manter todos os dados e a lógica necessários para executar uma interface de usuário interna ou externa totalmente interativa no banco de dados de instalação. A seção de referência descreve os elementos da interface do usuário que podem ser especificadas nas tabelas de banco de dados, incluindo caixas de diálogo, controles e eventos de controle.
-   As [ações padrão](standard-actions.md) discute as ações padrão usadas pelo instalador nas tabelas de sequência para executar uma instalação. Essas informações são destinadas principalmente a desenvolvedores de pacotes.
-   [Ações personalizadas](custom-actions.md) descreve como criar funcionalidades adicionais no instalador. As ações personalizadas permitem que um autor de um pacote de instalação estenda os recursos das ações padrão, incluindo executáveis, bibliotecas de vínculo dinâmico e script. Essas informações são destinadas a desenvolvedores de pacotes que precisam executar funções de instalação não encontradas em outro lugar do instalador.
-   [Propriedades](properties.md) fornece informações sobre as propriedades que o instalador usa durante uma instalação. As seções about e using fornecem uma visão geral dessas variáveis globais e cada propriedade é descrita na seção de referência.
-   [Fluxo de informações de resumo](summary-information-stream.md) documenta as propriedades de informações de resumo usadas pelo instalador. Essas informações são interessantes para todos os desenvolvedores.
-   A [aplicação de patches e atualizações](patching-and-upgrades.md) aborda o uso do instalador para executar atualizações de arquivos, QFEs, atualizações secundárias, atualizações de produtos e aplicação de patches.
-   As [transformações](transforms.md) explicam como alterar ou personalizar um banco de dados de instalação usando uma transformação de banco de dados e como gerar, proteger e aplicar transformações.
-   A [validação de pacote](package-validation.md) aborda o uso de avaliadores de consistência internos (ICES) para testar a consistência interna dos pacotes de instalação que estão em desenvolvimento.
-   Os [módulos de mesclagem](merge-modules.md) apresentam um padrão para o design de módulos de mesclagem. Esse padrão deve ser seguido por desenvolvedores que estão criando seus próprios módulos de mesclagem, bem como por desenvolvedores que planejam usar o instalador para fornecer código compartilhado para seus aplicativos.
-   [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md) discute como usar Windows Installer para instalar e gerenciar os componentes do instalador projetados para serem executados em sistemas operacionais de 64 bits.
-   [Windows Installer exemplos](windows-installer-examples.md) inclui um exemplo passo a passo de como criar um pacote de instalação com uma interface do usuário interna em [um exemplo de instalação](an-installation-example.md). Para obter um exemplo de criação de uma atualização importante para um pacote existente, consulte [um exemplo de atualização](an-upgrade-example.md). Para saber como uma transformação personalização desabilita recursos e adiciona novos recursos, consulte [um exemplo de transformação personalização](a-customization-transform-example.md). Para obter um exemplo de como criar um pacote de patch que aplica uma pequena atualização a um pacote de instalação existente, consulte [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md). Para saber como localizar um pacote do instalador existente, consulte [um exemplo de localização](a-localization-example.md).
-   a [interface de automação](automation-interface.md) fornece informações aos desenvolvedores que desejam usar a Interface de automação do Windows Installer.
-   As [funções do instalador](installer-functions.md) descrevem as chamadas de função para a API do instalador. Essas são as funções que outros aplicativos chamam para acessar os serviços do instalador para instalar, manter ou remover aplicativos. As seções usando incluem discussões sobre como solicitar recursos, iniciar instalações e reinstalar componentes ausentes programaticamente. A seção de referência é o material de referência principal para as funções de serviço do instalador.
-   O [banco de dados do instalador](installer-database.md) discute o banco de dados de instalação. O instalador mantém todos os dados e a lógica necessários para uma instalação em um banco de dados relacional localizado em um arquivo de .msi. A seção About fornece uma visão geral dos diagramas de esquema para os principais grupos funcionais de tabelas do banco de dados. A seção usando aborda o trabalho com as mais importantes dessas tabelas. Essas seções contêm informações essenciais para os desenvolvedores que estão criando pacotes de instalação ou gravando ferramentas de criação de pacote. A seção de referência contém material de referência completo para cada tabela de banco de dados. Esta seção também contém a referência principal para cada uma das funções de banco de dados. As funções de banco de dados são usadas internamente pelo instalador para acessar o banco de dados e são basicamente interessantes para os desenvolvedores de ferramentas de criação de pacote do instalador.

 

 



