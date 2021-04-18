---
description: As seções a seguir apresentam um exemplo de criação de um pacote de atualização para o aplicativo descrito em um exemplo de instalação.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Um exemplo de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768487"
---
# <a name="an-upgrade-example"></a>Um exemplo de atualização

As seções a seguir apresentam um exemplo de criação de um pacote de atualização para o aplicativo descrito em [um exemplo de instalação](an-installation-example.md). Um exemplo de uma interface de usuário mínima para esse exemplo é fornecido nos [componentes SDK do Windows para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) como o arquivo Uisample.msi. Se você tiver o SDK, terá acesso a todas as ferramentas e dados necessários para reproduzir o pacote de instalação de exemplo, a interface do usuário e o pacote de atualização de exemplo.

Este exemplo ilustra como criar um pacote de Windows Installer que atualiza o produto hipotético MNP2000 para um novo produto chamado MNP2001. O pacote de atualização de exemplo aplica uma atualização importante para o produto que requer a alteração do código do produto. Para obter mais informações sobre atualizações principais, consulte o tópico sobre [atualizações importantes](major-upgrades.md) na seção [patches e atualizações](patching-and-upgrades.md) .

O pacote de atualização de exemplo tem as seguintes especificações:

-   Para se qualificar para receber essa atualização para o MNP2001, um usuário deve ter instalado anteriormente as versões 1,0 para 1,4 (inclusivas) do idioma inglês MNP2000 usando Windows Installer.
-   Quando um usuário tenta instalar o pacote de atualização, a funcionalidade de atualização do Windows Installer pesquisa o computador do usuário em busca de todos os produtos que se qualificam para a atualização.
-   Windows Installer migra todas as configurações de recurso do produto original para o produto atualizado.
-   O instalador remove todos os recursos obsoletos do computador do usuário.
-   O instalador instala todos os novos recursos que pertencem à atualização.
-   Uma desinstalação do pacote de atualização remove o produto do computador do usuário e não restaura a versão anterior do produto.
-   A atualização de exemplo atualiza atalhos para novos arquivos e recursos.

    [Planejando uma atualização principal](planning-a-major-upgrade.md)

    [Importando banco de dados de instalação original](importing-original-installation-database.md)

    [Atualizando a estrutura de diretório para uma atualização](updating-directory-structure-for-an-upgrade.md)

    [Atualizando arquivos e atributos de arquivo para uma atualização](updating-files-and-file-attributes-for-an-upgrade.md)

    [Atualizando componentes para uma atualização](updating-components-for-an-upgrade.md)

    [Atualizando recursos para uma atualização](updating-features-for-an-upgrade.md)

    [Atualizando atalhos para uma atualização](updating-shortcuts-for-an-upgrade.md)

    [Atualizando a tabela de atualização para uma atualização](updating-upgrade-table-for-an-upgrade.md)

    [Atualizando Propriedades para uma atualização](updating-properties-for-an-upgrade.md)

    [Atualizando tabelas de sequência para uma atualização](updating-sequence-tables-for-an-upgrade.md)

    [Atualizando informações de resumo para uma atualização](updating-summary-information-for-an-upgrade.md)

    [Validando uma atualização de instalação](validating-an-installation-upgrade.md)

 

 



