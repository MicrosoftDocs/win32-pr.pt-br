---
description: O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa serviços de componentes, em si, um front-end gráfico escrito sobre os objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatizando a administração do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089378"
---
# <a name="automating-com-administration"></a>Automatizando a administração do COM+

O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa serviços de componentes, em si, um front-end gráfico escrito sobre os objetos administrativos. Você pode usar esses objetos, fornecidos pela biblioteca de administração de serviços de componentes (COMAdmin), para automatizar todas as tarefas na administração de aplicativos e serviços COM+.

Os objetos COMAdmin permitem que você leia e grave informações armazenadas no catálogo COM+, o armazenamento de dados subjacente que contém todos os dados de configuração do COM+.

Você pode usar esses objetos para fazer o seguinte:

-   Criar e configurar aplicativos COM+.
-   Instalar e exportar aplicativos COM+ existentes.
-   Gerenciar aplicativos COM+ instalados.
-   Gerenciar e configurar serviços.
-   Administre remotamente os serviços de componentes em um computador diferente.

Você pode usar os objetos COMAdmin programáveis com qualquer linguagem compatível com a automação, como o Microsoft Visual Basic e Visual Basic Script. Você pode desenvolver scripts leves ou ferramentas de administração de uso geral. Por exemplo, você pode fazer o seguinte:

-   Gravar scripts para executar tarefas administrativas rotineiras.
-   Grave scripts para automatizar processos no desenvolvimento de aplicativos COM+.
-   Desenvolva ferramentas de finalidade geral para administrar e monitorar serviços de componentes.
-   Desenvolva executáveis de instalação para instalar e implantar seu aplicativo COM+.

A biblioteca COMAdmin fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0. A maioria dos códigos de administração do MTS 2,0 ainda funcionará, embora com algumas exceções. (Consulte [biblioteca de administração do MTS](mts-administration-library.md).)

Para automatizar a administração com eficiência, você deve estar familiarizado com as tarefas de Administração realizadas com a ferramenta administrativa serviços de componentes.

Para obter descrições completas dos objetos COMAdmin e das interfaces correspondentes, consulte a documentação de referência do COM+ para as seguintes classes e interfaces:

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Os tópicos a seguir nesta seção fornecem uma visão geral para automatizar a administração usando os objetos COMAdmin:

-   [Visão geral dos objetos COMAdmin](overview-of-the-comadmin-objects.md)
-   [Recuperando coleções no catálogo COM+](retrieving-collections-on-the-com--catalog.md)
-   [Definindo propriedades e salvando alterações no catálogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Manipulando erros de administração COM+](handling-com--administration-errors.md)
-   [Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
-   [Exemplo introdutório usando o catálogo de administração do COM+](introductory-example-using-the-com--administration-catalog.md)

 

 



