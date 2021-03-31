---
title: Publicando em um contêiner do sistema de domínio
description: O contêiner do sistema de uma partição de domínio contém informações operacionais por domínio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicando em um contêiner do sistema de domínio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822255"
---
# <a name="publishing-in-a-domain-system-container"></a>Publicando em um contêiner do sistema de domínio

O contêiner do sistema de uma partição de domínio contém informações operacionais por domínio. Isso inclui a política de segurança local padrão, rastreamento de link de arquivo, reuniões de rede e contêineres para pontos de conexão de RnR (registro e resolução do Windows Sockets) e serviço de nome RPC (RpcNs). O contêiner do sistema está oculto, por padrão, e fornece um local conveniente para armazenar objetos de interesse para os administradores, mas não para os usuários finais.

Os serviços que não estão vinculados a um único host podem querer criar seus SCPs no contêiner do sistema de uma partição de domínio. Essa alternativa pode ser útil para serviços com réplicas instaladas em vários hosts, cada réplica fornecendo serviços idênticos aos clientes em todo o domínio. Ele permite agrupar todos os objetos para o serviço replicado em um único contêiner.

Os serviços que criam objetos específicos do serviço no contêiner do sistema devem fazer o seguinte:

1.  Crie um subcontêiner do **contêiner** da classe de objeto como um filho imediato do contêiner do sistema. Dê a esse subcontêiner um nome que o identifique claramente como pertencente ao serviço.
2.  Crie os objetos relacionados ao serviço nesse subcontêiner. Por exemplo, o NetMeeting usa o contêiner de reuniões para publicar objetos de reunião de rede.

Um fornecedor com vários produtos pode usar uma estratégia semelhante para agrupar objetos relacionados ao serviço para todos os seus produtos. Nesse caso, você pode criar um objeto de **contêiner** com um nome que identifique claramente o fornecedor; em seguida, crie objetos de **contêiner** para cada serviço como filhos do contêiner do fornecedor. Crie o contêiner específico do fornecedor como um filho do contêiner do sistema.

 

 




