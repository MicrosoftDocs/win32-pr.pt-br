---
description: Um pacote de instalação contém todas as informações que o Windows Installer requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacote de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748158"
---
# <a name="installation-package"></a>Pacote de instalação

Um pacote de instalação contém todas as informações que o Windows Installer requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação. Cada pacote de instalação inclui um arquivo. msi, que contém um banco de dados de instalação, um fluxo de informações resumido e os data streams para várias partes da instalação. O arquivo. msi também pode conter uma ou mais transformações, arquivos de origem internos e arquivos de origem externos ou arquivos de gabinete exigidos pela instalação.

Os desenvolvedores de aplicativos devem criar uma instalação para usar o instalador. Como o instalador organiza as instalações em torno do conceito de [componentes e recursos](components-and-features.md)e armazena todas as informações sobre a instalação em um banco de dados relacional, o processo de criação de um pacote de instalação envolve amplamente as seguintes etapas:

-   Identifique os recursos a serem apresentados aos usuários.
-   Organize o aplicativo em componentes.
-   Preencha o banco de dados de instalação com informações.
-   Valide o pacote de instalação.

A próxima seção aborda os componentes e recursos do instalador. Para obter mais informações, consulte [componentes e recursos](components-and-features.md). A escolha dos recursos é normalmente determinada pela funcionalidade do aplicativo da perspectiva do usuário.

É recomendável que os desenvolvedores usem um procedimento padrão para escolher componentes. Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md).

Os autores de pacote podem usar ferramentas de criação de pacote de terceiros ou um editor de tabela e o SDK do Windows Installer para preencher o banco de dados de instalação. Todos os pacotes de instalação precisam ser validados para consistência interna. Para obter mais informações, consulte [validação de pacote](package-validation.md).

 

 



