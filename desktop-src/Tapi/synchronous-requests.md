---
description: Os designers do provedor de serviços devem tentar manter o tempo de execução de operações síncronas curtas.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Solicitações síncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e399fcef1ffba574305b70aee05d7430bcd84746458198b3d33ed6bb0848747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760681"
---
# <a name="synchronous-requests"></a>Solicitações síncronas

Os designers do provedor de serviços devem tentar manter o tempo de execução de operações síncronas curtas. Por exemplo, há uma operação "Aberta" chamada no momento da inicialização que prepara o provedor de serviços e a TAPI para operações subsequentes em um dispositivo. Um provedor de serviços cuja implementação é dividida entre o computador cliente e um servidor dedicado pode ter uma confiança razoável de que ele pode se comunicar com seu servidor remoto. Sua implementação de "Abrir" pode apenas alocar e inicializar estruturas de dados para representar o dispositivo e retornar, acionando a comunicação de ponta a ponta até que alguma operação real seja solicitada.

Qualquer implementação "otimista" de uma operação síncrona pode encontrar mais tarde limitações de recursos ou falhas de comunicação remota. Em geral, até mesmo uma abordagem "conservadora" não pode impedir totalmente esses problemas; os designers de provedor de serviços devem escolher a melhor troca entre confiabilidade e desempenho. Uma falha desse tipo deve ser tratada normalmente sempre que possível. Do ponto de vista dos dispositivos TSPI, eles devem permanecer válidos para fins de "contabilidade", mesmo que retornem o status de falha para qualquer operação solicitada.

A implementação de uma abordagem otimista para solicitações síncronas não deve ser feita às custas da semântica correta para a operação. Retornando ao exemplo de "Abrir", se a abertura de um dispositivo precisar competir e reservar um recurso raro e não compartilhamento, como portas de comunicação, ele provavelmente deverá fazer isso mesmo que seja demorado.

**TAPI 2.x:** Uma operação que é concluída de forma síncrona executa todo o processamento na chamada de função feita pelo aplicativo. A função retorna valores diferentes dependendo de seu sucesso ou falha:

-   **Sucesso síncrono.** Se a solicitação ou o serviço correspondente à função tiver sido executado com êxito, a função retornará zero, indicando êxito. Todos os valores gravados como resultado da chamada de função são confiáveis e podem ser usados imediatamente.
-   **Falha síncrona.** Se a função detectar um erro e a solicitação não for executada, um número de erro negativo será retornado para identificar o erro.

 

 



