---
title: Publicando em um contêiner do sistema de domínio
description: O contêiner system de uma partição de domínio contém informações operacionais por domínio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicando em um AD de contêiner do sistema de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb86a49bb14bc88d64a723ca9ab289723ff4ac2b9259f112323e19a04497362c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184950"
---
# <a name="publishing-in-a-domain-system-container"></a>Publicando em um contêiner do sistema de domínio

O contêiner system de uma partição de domínio contém informações operacionais por domínio. Isso inclui a política de segurança local padrão, o acompanhamento de link de arquivo Windows, reuniões de rede e contêineres para pontos de conexão de RnR (registro e resolução de soquetes) e RPC (serviço de nome RPC). O contêiner do sistema fica oculto, por padrão, e fornece um local conveniente para armazenar objetos que são de interesse dos administradores, mas não para os usuários finais.

Os serviços que não estão vinculados a um único host podem querer criar seus SCPs no contêiner Sistema de uma partição de domínio. Essa alternativa pode ser útil para serviços com réplicas instaladas em vários hosts, cada réplica fornecendo serviços idênticos aos clientes em todo o domínio. Ele permite agrupar todos os objetos para o serviço replicado em um único contêiner.

Os serviços que criam objetos específicos do serviço no contêiner Sistema devem fazer o seguinte:

1.  Crie um subcon contêiner do contêiner de classe de **objeto** como um filho imediato do contêiner System. Dê a esse subcon contêiner um nome que o identifique claramente como pertencente ao serviço.
2.  Crie os objetos relacionados ao serviço neste subcon contêiner. Por exemplo, NetMeeting usa o contêiner Meetings para publicar objetos de reunião de rede.

Um fornecedor com vários produtos pode usar uma estratégia semelhante para agrupar objetos relacionados ao serviço para todos os seus produtos. Nesse caso, você pode criar um objeto **de** contêiner com um nome que identifique claramente o fornecedor; em **seguida, crie objetos** de contêiner para cada serviço como filhos do contêiner do fornecedor. Crie o contêiner específico do fornecedor como um filho do contêiner Do sistema.

 

 




