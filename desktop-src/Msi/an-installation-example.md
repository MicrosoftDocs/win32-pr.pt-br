---
description: Este exemplo ilustra como criar um pacote Windows Installer simples que instala um aplicativo.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Um exemplo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828076"
---
# <a name="an-installation-example"></a>Um exemplo de instalação

Este exemplo ilustra como criar um pacote Windows Installer simples que instala um aplicativo. O exemplo instala o bloco de notas, um editor de texto incluído no Windows e vários arquivos de texto que descrevem eventos e admissões na arena de parque vermelho imaginário.

O exemplo tem as seguintes especificações:

-   O aplicativo é fornecido aos usuários como um pacote de Windows Installer de instalação automática que instala todos os arquivos, atalhos e informações de registro necessários.
-   O pacote de instalação pode apresentar um assistente de interface de usuário ao usuário durante a instalação para coletar informações do usuário.
-   Durante a instalação, os usuários têm a opção de selecionar recursos individuais a serem instalados para execução local, para execução a partir de origem ou para não ser instalado.
-   Um dos recursos pode ser apresentado aos usuários como um recurso de instalação sob demanda.
-   O mesmo pacote desinstala o aplicativo e remove todos os arquivos de aplicativo e informações de registro do computador do usuário.
-   O pacote está preparado para receber uma atualização importante que inclui a alteração do código do produto.

Para reproduzir o exemplo, você precisa de uma ferramenta de software capaz de criar e editar um banco de dados Windows Installer em branco. Várias ferramentas de criação de pacote estão disponíveis de fornecedores de software independentes. Um editor de banco de dados Windows Installer chamado Orca é fornecido no [SDK do Windows components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Para concluir o exemplo, siga estas etapas:

[Planejando a instalação](planning-the-installation.md)

[Importando um banco de dados em branco](importing-a-blank-database.md)

[Especificando a estrutura do diretório](specifying-directory-structure.md)

[Especificando componentes](specifying-components.md)

[Especificando arquivos e atributos de arquivo](specifying-files-and-file-attributes.md)

[Especificando a mídia de origem](specifying-source-media.md)

[Especificando recursos](specifying-features.md)

[Especificando relações de Feature-Component](specifying-feature-component-relationships.md)

[Adicionando informações do registro](adding-registry-information.md)

[Especificando atalhos](specifying-shortcuts.md)

[Especificando propriedades](specifying-properties.md)

[Importando o InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importando o InstallUISequence](importing-the-installuisequence.md)

[Importando o AdminExecuteSequence](importing-the-adminexecutesequence.md)

[Importando o AdminUISequence](importing-the-adminuisequence.md)

[Importando o AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Adicionando informações de resumo](adding-summary-information.md)

[Importando a interface do usuário](importing-the-user-interface.md)

[Validando um banco de dados de instalação](validating-an-installation-database.md)

 

 



