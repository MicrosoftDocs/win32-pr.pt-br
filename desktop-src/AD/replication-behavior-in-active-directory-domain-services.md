---
title: Comportamento de replicação no Active Directory Domain Services
description: O comportamento de replicação é consistente e previsível; dado um conjunto de alterações em uma determinada réplica, o resultado pode ser previsto \ 8212; as alterações serão propagadas para todas as outras réplicas.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822253"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportamento de replicação no Active Directory Domain Services

O comportamento de replicação é consistente e previsível; dado um conjunto de alterações em uma determinada réplica, o resultado pode ser previsto — as alterações serão propagadas para todas as outras réplicas. É impossível planejar um modelo geral confiável para prever quando as alterações serão aplicadas em todas as outras réplicas ou em uma réplica específica, pois o estado futuro do sistema distribuído como um todo não pode ser conhecido. Isso é chamado de "latência não determinística" e os aplicativos que usam o diretório devem entender e permitir.

A situação não é tão complexa quanto pode ser exibida. Há apenas três Estados que um aplicativo deve acomodar:

-   Distorção de versão: nenhuma das alterações aplicadas a uma determinada réplica de origem foi propagada para uma determinada réplica de destino. Um aplicativo que lê a réplica de origem vê a nova versão das informações, enquanto um aplicativo que lê o destino vê a versão antiga (ou nada, se as novas informações foram adicionadas pela primeira vez). A distorção de versão se aplica a todos os consumidores do serviço de diretório.
-   Atualização parcial: algumas das alterações aplicadas a uma determinada réplica de origem foram propagadas para uma determinada réplica de destino. Um aplicativo que lê a réplica de origem vê as novas informações, enquanto um aplicativo que lê o destino vê uma mistura de informações novas e antigas (ou apenas algumas das novas informações, se as novas informações foram adicionadas pela primeira vez). A atualização parcial se aplica aos consumidores do serviço de diretório que usam dois ou mais objetos relacionados para armazenar suas informações.
-   Estado totalmente replicado: todas as alterações aplicadas a uma determinada réplica de origem foram propagadas para uma determinada réplica de destino. Os aplicativos nas réplicas de origem e de destino veem as mesmas informações.

 

 




