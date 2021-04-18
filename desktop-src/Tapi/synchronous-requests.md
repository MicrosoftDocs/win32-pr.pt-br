---
description: Os designers do provedor de serviços devem tentar manter o tempo de execução das operações síncronas de forma curta.
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: Solicitações síncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766964"
---
# <a name="synchronous-requests"></a>Solicitações síncronas

Os designers do provedor de serviços devem tentar manter o tempo de execução das operações síncronas de forma curta. Por exemplo, há uma operação "aberta" chamada no momento da inicialização que prepara o provedor de serviços e a TAPI para operações subsequentes em um dispositivo. Um provedor de serviços cuja implementação é dividida entre o computador cliente e um servidor dedicado pode ter confiança razoável de que ele pode se comunicar com seu servidor remoto. Sua implementação de "Open" pode simplesmente alocar e inicializar estruturas de dados para representar o dispositivo e retornar, adiando a comunicação de ponta a ponta até que alguma operação real seja solicitada.

Qualquer implementação "otimista" de uma operação síncrona pode encontrar mais tarde as limitações de recursos ou falhas de comunicação remota. Em geral, até mesmo uma abordagem "conservadora" não pode impedir totalmente esses problemas; os designers do provedor de serviços devem escolher a melhor compensação entre confiabilidade e desempenho. Uma falha desse tipo deve ser tratada normalmente sempre que possível. Do ponto de vista dos dispositivos TSPI, eles devem permanecer válidos para fins de "escrituração", mesmo que retornem o status de falha para qualquer operação solicitada.

A implementação de uma abordagem otimista para solicitações síncronas não deve ser feita às custas da semântica correta para a operação. Retornando ao exemplo "Open", se abrir um dispositivo precisar competir e reservar um recurso escasso e não compartilhável, como as portas de comunicação, ele provavelmente deve fazer isso mesmo que seja demorado.

**TAPI 2. x:** Uma operação que é concluída de forma síncrona executa todo o seu processamento na chamada de função feita pelo aplicativo. A função retorna valores diferentes dependendo de seu sucesso ou falha:

-   **Êxito síncrono.** Se a solicitação ou o serviço correspondente à função tiver sido executado com êxito, a função retornará zero, indicando êxito. Todos os valores gravados como resultado da chamada de função são confiáveis e podem ser usados imediatamente.
-   **Falha síncrona.** Se a função detectar um erro e a solicitação não for executada, um número de erro negativo será retornado para identificar o erro.

 

 



