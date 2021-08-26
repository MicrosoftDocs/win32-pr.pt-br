---
description: O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa dos Serviços de Componentes, um front-end gráfico escrito sobre os objetos administrativos.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatizando a administração COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cb7370c3b1a90324b612108e9ec1ef17c7030d3372d303da74ced95298ab02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029836"
---
# <a name="automating-com-administration"></a>Automatizando a administração COM+

O COM+ fornece um modelo de objeto de administração que expõe toda a funcionalidade da ferramenta administrativa dos Serviços de Componentes, um front-end gráfico escrito sobre os objetos administrativos. Você pode usar esses objetos, fornecidos pela biblioteca COMAdmin (Administração de Serviços de Componentes), para automatizar todas as tarefas na administração de aplicativos e serviços COM+.

Os objetos COMAdmin permitem que você leia e escreva informações armazenadas no catálogo COM+, o armazenamento de dados subjacente que contém todos os dados de configuração COM+.

Você pode usar esses objetos para fazer o seguinte:

-   Criar e configurar aplicativos COM+.
-   Instalar e exportar aplicativos COM+ existentes.
-   Gerenciar aplicativos COM+ instalados.
-   Gerenciar e configurar serviços.
-   Administrar remotamente os Serviços de Componentes em um computador diferente.

Você pode usar os objetos COMAdmin que podem ser scripts com qualquer linguagem compatível com a Automação, como o Microsoft Visual Basic e Visual Basic Script. Você pode desenvolver scripts leves ou ferramentas de administração de uso geral. Por exemplo, você pode fazer o seguinte:

-   Escreva scripts para executar tarefas administrativas rotineiras.
-   Escreva scripts para automatizar processos no desenvolvimento de aplicativos COM+.
-   Desenvolva ferramentas de uso geral para administrar e monitorar os Serviços de Componentes.
-   Desenvolva executáveis de instalação para instalar e implantar seu aplicativo COM+.

A Biblioteca COMAdmin fornece compatibilidade com compatibilidade com a Biblioteca de Administração do MTS 2.0. A maioria do código de administração do MTS 2.0 existente ainda funcionará, embora com algumas exceções. (Consulte [Biblioteca de Administração do MTS](mts-administration-library.md).)

Para automatizar a administração com eficiência, você deve estar familiarizado com as tarefas de administração, conforme executado com a ferramenta administrativa dos Serviços de Componentes.

Para ver descrições completas dos objetos COMAdmin e das interfaces correspondentes, consulte a documentação de Referência do COM+ para as seguintes classes e interfaces:

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
-   [Tratando erros de administração COM+](handling-com--administration-errors.md)
-   [Operações de administração COM+ em transações](com--administration-operations-within-transactions.md)
-   [Exemplo introdutório usando o catálogo de administração COM+](introductory-example-using-the-com--administration-catalog.md)

 

 



