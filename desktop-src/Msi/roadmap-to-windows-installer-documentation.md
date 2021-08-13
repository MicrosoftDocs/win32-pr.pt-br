---
description: Esta documentação é a principal fonte de material de referência para Windows Instalador.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Roteiro para a documentação Windows instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625906"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Roteiro para a documentação Windows instalador

Esta documentação é a principal fonte de material de referência para Windows Instalador. Ele fornece informações sobre pacotes de instalação e o serviço do instalador. Ele também fornece descrições completas da API (interface de programação de aplicativo) e dos elementos do banco de dados do instalador. Esta documentação também contém uma discussão sobre exemplos básicos de instalação e atualização de pacotes [no Windows do Instalador.](windows-installer-examples.md)

O Guia baseado em função para Windows [documentação](role-based-guide-to-windows-installer-documentation.md) do instalador é uma alternativa fornecida como um guia para leitores que preferem ver links para tópicos organizados por cenários de tarefas comuns e de função profissional.

Para obter informações sobre Windows grupos de notícias do Instalador do Windows, consulte também o tópico: Outras [fontes do Windows informações do instalador.](other-sources-of-windows-installer-information.md)

Para ver uma lista de dicas sobre como usar o instalador Windows, consulte Práticas recomendadas do Windows [Instalador.](windows-installer-best-practices.md)

A lista a seguir descreve cada seção da documentação do instalador.

-   [Sobre Windows Installer](about-windows-installer.md) fornece uma visão geral dos recursos e benefícios do instalador, como anúncio, instalação sob demanda, resiliência, personalização e gerenciamento de componentes. Esta seção apresenta os conceitos de componentes e recursos do instalador, que são essenciais para entender como o instalador organiza uma instalação. Ele também aborda vários assuntos de alto nível sobre a instalação, como Política do Sistema, Regras de Versão de Arquivo e Instalação de Reversões.
-   [O Windows Installer](using-windows-installer.md) discute uma variedade de tópicos, como um método padrão para organizar um aplicativo em componentes que o instalador pode instalar ou remover do computador do usuário; como baixar um pacote de instalação do World Wide Web; e usando imagens de origem compactadas.
-   As informações nas seções Novidades do [Windows Installer](what-s-new-in-windows-installer.md) podem ser usadas para identificar novos recursos que não são suportados por versões anteriores Windows Installer.
-   [Assinaturas Digitais e Windows Instalador](digital-signatures-and-windows-installer.md) de Arquivos descreve como as assinaturas digitais podem ser usadas com pacotes, transformaçãos, patches, módulos de mesclagem e arquivos de gabinete externos.
-   [Os assemblies](assemblies.md) explicam como usar o Windows Instalador para instalar e gerenciar o Common Language Run Time e assemblies Win32.
-   [Interface do Usuário](user-interface.md) fornece informações sobre os recursos de interface do usuário do instalador. Embora o instalador não forneça uma interface do usuário, um autor do pacote pode manter todos os dados e a lógica necessários para executar uma interface do usuário interna ou externa totalmente interativa no banco de dados de instalação. A seção Referência descreve elementos da interface do usuário que são especificados nas tabelas de banco de dados, incluindo caixas de diálogo, controles e eventos de controle.
-   [As Ações](standard-actions.md) Padrão discutem as ações padrão usadas pelo instalador nas tabelas de sequência para executar uma instalação. Essas informações são destinadas principalmente a desenvolvedores de pacotes.
-   [Ações personalizadas](custom-actions.md) descreve como criar funcionalidades adicionais no instalador. As ações personalizadas permitem que um autor de um pacote de instalação estenda os recursos das ações padrão, incluindo executáveis, bibliotecas de vínculo dinâmico e script. Essas informações são destinadas a desenvolvedores de pacotes que precisam executar funções de instalação não encontradas em outro lugar no instalador.
-   [As](properties.md) propriedades fornece informações sobre as propriedades que o instalador usa durante uma instalação. As seções Sobre e Usando fornece uma visão geral dessas variáveis globais e cada propriedade é descrita na seção Referência.
-   [Summary Information Stream](summary-information-stream.md) documenta as propriedades de informações de resumo usadas pelo instalador. Essas informações são de interesse de todos os desenvolvedores.
-   [A a patch e as atualizações](patching-and-upgrades.md) discutem o uso do instalador para executar atualizações de arquivo, QFEs, atualizações secundárias, atualizações de produtos e a a patch.
-   [As transformaçãos](transforms.md) explicam como alterar ou personalizar um banco de dados de instalação usando uma transformação de banco de dados e como gerar, proteger e aplicar as transformação.
-   [A Validação](package-validation.md) de Pacote discute o uso de ICEs (Avaliadores de Consistência Interna) para testar a consistência interna dos pacotes de instalação que estão em desenvolvimento.
-   [Os Módulos de](merge-modules.md) Mesclagem apresentam um padrão para o design de módulos de mesclagem. Esse padrão deve ser seguido por desenvolvedores que estão criando seus próprios módulos de mesclagem, bem como por desenvolvedores que planejam usar o instalador para fornecer código compartilhado para seus aplicativos.
-   Windows Instalador em Sistemas Operacionais de [64](windows-installer-on-64-bit-operating-systems.md) bits discute como usar o Windows Installer para instalar e gerenciar componentes do instalador projetados para ser executado em sistemas operacionais de 64 bits.
-   [Windows Exemplos](windows-installer-examples.md) do Instalador do Windows inclui um exemplo passo a passo da criação de um pacote de instalação com uma interface do usuário interna em Um exemplo [de instalação.](an-installation-example.md) Para ver um exemplo de como fazer uma atualização principal para um pacote existente, consulte [Um exemplo de atualização](an-upgrade-example.md). Para saber como uma transformação de personalização desabilita recursos e adiciona novos recursos, consulte [Um exemplo de transformação de personalização](a-customization-transform-example.md). Para ver um exemplo de criação de um pacote de patch que aplica uma pequena atualização a um pacote de instalação existente, consulte [Exemplo de Aplicação](a-small-update-patching-example.md)de Patch de Pequena Atualização . Para saber como localizar um pacote do instalador existente, consulte [Um exemplo de localização](a-localization-example.md).
-   [A Interface de](automation-interface.md) Automação fornece informações aos desenvolvedores que querem usar a interface de automação do Windows Installer.
-   [O Installer Functions](installer-functions.md) descreve chamadas de função para a API do instalador. Essas são as funções que outros aplicativos chamam para acessar os serviços do instalador para instalar, manter ou remover aplicativos. As seções Usando incluem discussões sobre como solicitar recursos, iniciar instalações e reinstalar componentes ausentes programaticamente. A seção Referência é o material de referência principal para as funções de serviço do instalador.
-   [O Banco de Dados do Instalador](installer-database.md) discute o banco de dados de instalação. O instalador mantém toda a lógica e os dados necessários para uma instalação em um banco de dados relacional localizado em um arquivo .msi dados. A seção Sobre fornece uma visão geral com diagramas de esquema para os principais grupos funcionais de tabelas do banco de dados. A seção Uso aborda como trabalhar com as tabelas mais importantes. Essas seções contêm informações essenciais para desenvolvedores que estão criar pacotes de instalação ou escrever ferramentas de criação de pacote. A seção Referência contém o material de referência completo para cada tabela de banco de dados. Esta seção também contém a referência primária para cada uma das funções de banco de dados. As funções de banco de dados são usadas internamente pelo instalador para acessar o banco de dados e são de interesse principalmente para desenvolvedores de ferramentas de criação de pacote do instalador.

 

 



