---
description: O Windows Installer reduz o TCO (custo total de propriedade) de seus aplicativos, aumentando a capacidade de seus clientes de gerenciar e manter componentes de aplicativos durante a instalação e o tempo de execução.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Gerenciamento de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780521"
---
# <a name="component-management"></a>Gerenciamento de componentes

O Windows Installer reduz o TCO (custo total de propriedade) de seus aplicativos, aumentando a capacidade de seus clientes de gerenciar e manter componentes de aplicativos durante a instalação e o tempo de execução. O banco de dados de instalação rastreia quais aplicativos exigem um componente específico, quais arquivos compõem cada componente, onde cada arquivo é instalado no sistema e onde as origens do componente estão localizadas. Isso permite que os desenvolvedores criem pacotes que fornecem os seguintes benefícios:

-   Maior resiliência dos aplicativos. Use o instalador para detectar e reinstalar componentes danificados sem precisar executar a instalação novamente. O instalador verifica o caminho de um componente em tempo de execução. Isso libera aplicativos da dependência de caminhos de arquivo estáticos que normalmente são diferentes entre computadores e podem apontar para componentes ausentes. Para obter mais informações, consulte [resiliência](resiliency.md).
-   Instalação sob demanda. Esse conjunto de recursos não é instalado durante a instalação, mas é especificado no banco de dados a ser instalado just-in-time para uso, se exigido pelo aplicativo no futuro. Os usuários não precisam executar a instalação novamente. Para obter mais informações, consulte [instalação sob demanda](installation-on-demand.md).
-   Anúncio de atalhos para recursos, aplicativos ou produtos inteiros na interface do usuário. Os usuários podem instalá-los sob demanda usando os atalhos. Os usuários também podem remover recursos, aplicativos ou produtos inteiros sob demanda. Para obter mais informações, consulte [anúncio](advertisement.md).
-   Personalização da instalação. Um administrador pode aplicar transformações ao banco de dados que personalizam a instalação de um grupo específico de usuários. Para obter mais informações, confira [Personalização](customization.md).
-   Implantação mais fácil de atualizações de aplicativos. Use o instalador para atualizar seus produtos. Para obter mais informações, consulte [patches e atualizações](patching-and-upgrades.md).
-   Exibição de atalho de recurso. O instalador exibe atalhos para recursos executados localmente com atalhos para recursos que são executados remotamente. Como o banco de dados de instalação especifica o contexto de execução de cada recurso, pontos de entrada equivalentes visivelmente podem ser apresentados aos usuários conforme necessário.
-   Manter métricas de uso em recursos. Os desenvolvedores podem fornecer um pacote de instalação que mantém a contagem de uso de um recurso por todos os aplicativos cliente e remove componentes que não estão sendo usados.
-   Incorpore instalações. Os desenvolvedores podem incorporar os recursos de gerenciamento de componentes do instalador em seus aplicativos, criando um pacote de instalação e usando as [funções do instalador](installer-functions.md) no código do aplicativo. A figura a seguir ilustra um aplicativo que solicita a instalação de um recurso.

    ![aplicativo solicitando a instalação do recurso. ](images/over1.png)

 

 



