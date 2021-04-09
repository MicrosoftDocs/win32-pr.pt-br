---
description: COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: O utilitário de replicação COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920512"
---
# <a name="the-comrepl-replication-utility"></a>O utilitário de replicação COMREPL

COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino. Imagine o computador de origem que representa uma "configuração mestra". COMREPL é usado para replicar essa configuração mestre para manter um conjunto de computadores configurados de forma idêntica.

A unidade de replicação é a configuração COM+ inteira no computador mestre. Todos os aplicativos COM+ no mestre são replicados para os computadores de destino; é tudo ou nada. Além disso, todos os aplicativos COM+ instalados anteriormente nos computadores de destino, com exceção dos aplicativos pré-instalados em COM+, serão excluídos como parte do processo de replicação.

COMREPL replica somente os dados de configuração do COM+. Isso inclui aplicativos COM+ e configurações de computador específicas do COM+. O Microsoft Serviços de Informações da Internet (IIS) tem um utilitário semelhante (IISSync), que utiliza o COMREPL para replicar a configuração do IIS e do COM+.

Para obter informações detalhadas sobre como iniciar e usar o COMREPL, consulte os seguintes tópicos nesta seção:

-   [Usando COMREPL](using-comrepl.md)
-   [O que é replicado](what-gets-replicated.md)
-   [Fases de replicação](replication-phases.md)
-   [Gerenciamento de Arquivos](file-management.md)
-   [Registro em log e relatório de erros](logging-and-error-reporting.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando pacotes de instalação para aplicativos COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implantando proxies de aplicativo](deploying-application-proxies.md)
</dt> <dt>

[O catálogo COM+](the-com--catalog.md)
</dt> </dl>

 

 



