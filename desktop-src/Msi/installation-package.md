---
description: Um pacote de instalação contém todas as informações que o instalador Windows requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacote de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633816"
---
# <a name="installation-package"></a>Pacote de instalação

Um pacote de instalação contém todas as informações que o instalador Windows requer para instalar ou desinstalar um aplicativo ou produto e executar a interface do usuário de instalação. Cada pacote de instalação inclui um arquivo .msi, contendo um banco de dados de instalação, um fluxo de informações de resumo e fluxos de dados para várias partes da instalação. O .msi arquivo também pode conter uma ou mais transformaçãos, arquivos de origem internos e arquivos de origem externos ou arquivos de gabinete exigidos pela instalação.

Os desenvolvedores de aplicativos devem fazer uma instalação para usar o instalador. Como o instalador organiza instalações em [](components-and-features.md)torno do conceito de componentes e recursos e armazena todas as informações sobre a instalação em um banco de dados relacional, o processo de autor de um pacote de instalação envolve amplamente as seguintes etapas:

-   Identifique os recursos a serem apresentados aos usuários.
-   Organize o aplicativo em componentes.
-   Preencha o banco de dados de instalação com informações.
-   Valide o pacote de instalação.

A próxima seção aborda os componentes e os recursos do instalador. Para obter mais informações, consulte [Componentes e recursos](components-and-features.md). A escolha de recursos normalmente é determinada pela funcionalidade do aplicativo da perspectiva do usuário.

É recomendável que os desenvolvedores usem um procedimento padrão para escolher componentes. Para obter mais informações, consulte [Organizando aplicativos em componentes](organizing-applications-into-components.md).

Os autores de pacote podem usar ferramentas de criação de pacote de terceiros ou um editor de tabelas e o SDK do Windows Installer para popular o banco de dados de instalação. Todos os pacotes de instalação precisam ser validados para consistência interna. Para obter mais informações, consulte [Validação de pacote](package-validation.md).

 

 



