---
description: COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: O utilitário de replicação COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446cfc0e627463e8c142ccab624c3773123034c2becebc402a6069f74d30ccd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305291"
---
# <a name="the-comrepl-replication-utility"></a>O utilitário de replicação COMREPL

COMREPL é um utilitário que replicará o catálogo COM+ de um determinado computador de origem para um ou mais computadores de destino. Pense no computador de origem que representa uma "configuração mestra". COMREPL é usado para replicar essa configuração mestra para manter um conjunto de computadores configurados de forma idêntica.

A unidade de replicação é toda a configuração COM+ no computador mestre. Todos os aplicativos COM+ no mestre são replicados para os computadores de destino; é tudo ou nada. Além disso, todos os aplicativos COM+ instalados anteriormente nos computadores de destino, com exceção dos aplicativos pré-instalados COM+, serão excluídos como parte do processo de replicação.

COMREPL replica apenas dados de configuração COM+. Isso inclui aplicativos COM+ e configurações de computador específicas do COM+. Serviços de Informações da Internet da Microsoft (IIS) tem um utilitário semelhante (IISSync), que usa COMREPL para replicar a configuração de IIS e COM+.

Para obter informações detalhadas sobre como iniciar e usar COMREPL, consulte os seguintes tópicos nesta seção:

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

 

 



