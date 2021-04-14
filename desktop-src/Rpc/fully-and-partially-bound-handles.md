---
title: Identificadores totalmente e parcialmente ligados
description: Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de execução obtêm as informações de Endpoint conforme elas precisam.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453616"
---
# <a name="fully-and-partially-bound-handles"></a>Identificadores totalmente e parcialmente ligados

Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de execução obtêm as informações de Endpoint conforme elas precisam. As bibliotecas de tempo de execução fazem a distinção entre um *identificador totalmente associado* (um que inclui informações de ponto de extremidade) e um *identificador parcialmente associado* (um que não inclui informações de ponto de extremidade).

A biblioteca de tempo de execução do cliente deve converter o identificador parcialmente associado em um identificador totalmente associado antes que o cliente possa se associar ao servidor. A biblioteca de tempo de execução do cliente tenta converter o identificador de associação parcial para o aplicativo cliente obtendo as informações do ponto de extremidade conforme mostrado:

-   Da especificação da interface do cliente
-   De um serviço de mapeamento de ponto de extremidade em execução no servidor

Se o cliente tentar usar um identificador parcialmente associado quando as informações do ponto de extremidade não estiverem disponíveis na especificação de interface e o mapeador de ponto de extremidade do servidor não tiver informações sobre o ponto de extremidade do servidor, o cliente não terá informações suficientes para fazer sua chamada de procedimento remoto e essa chamada falhará. Para evitar isso, você deve registrar o ponto de extremidade no mapeador de ponto de extremidade quando seu aplicativo distribuído usa identificadores parcialmente associados. Para obter mais informações sobre o mapeador de ponto de extremidade, consulte [especificando pontos de extremidades dinâmicos](specifying-endpoints.md).

Quando uma chamada de procedimento remoto falha, o aplicativo cliente pode chamar [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para remover informações de ponto de extremidade desatualizadas. Quando o cliente tenta chamar o procedimento remoto, a biblioteca de tempo de execução do cliente tenta novamente converter o identificador totalmente associado em um identificador parcialmente associado. Isso é útil quando o servidor foi interrompido e reiniciado usando um ponto de extremidade dinâmico diferente.

 

 




