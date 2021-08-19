---
title: Alças totalmente e parcialmente vinculadas
description: Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de run-time obtém informações de ponto de extremidade conforme elas precisam.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f711955cedfba4359b910271f3ec5d77f4b383017eed8144e5201bb2d11cd3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929644"
---
# <a name="fully-and-partially-bound-handles"></a>Alças totalmente e parcialmente vinculadas

Quando você usa pontos de extremidade dinâmicos, as bibliotecas de tempo de run-time obtém informações de ponto de extremidade conforme elas precisam. As bibliotecas de tempo de run-time fazem *a* distinção entre um alça totalmente vinculado (um que inclui informações de ponto de extremidade) e um alça parcialmente vinculado *(um* que não inclui informações de ponto de extremidade).

A biblioteca em tempo de run time do cliente deve converter o alça parcialmente vinculado em um alça totalmente vinculado antes que o cliente possa se vincular ao servidor. A biblioteca em tempo de run time do cliente tenta converter o handle parcialmente vinculado para o aplicativo cliente obtendo as informações do ponto de extremidade, conforme mostrado:

-   Na especificação da interface do cliente
-   De um serviço de mapeamento de ponto de extremidade em execução no servidor

Se o cliente tentar usar um alça parcialmente vinculado quando as informações do ponto de extremidade não estão disponíveis na especificação da interface e o mapeamento de ponto de extremidade do servidor não tiver informações sobre o ponto de extremidade do servidor, o cliente não terá informações suficientes para fazer sua chamada de procedimento remoto e essa chamada falhará. Para evitar isso, você deve registrar o ponto de extremidade no mapeado de ponto de extremidade quando seu aplicativo distribuído usa alças parcialmente vinculadas. Para obter mais informações sobre o mapeamento de ponto de extremidade, consulte [Especificando pontos de extremidade dinâmicos.](specifying-endpoints.md)

Quando uma chamada de procedimento remoto falha, o aplicativo cliente pode chamar [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para remover informações de ponto de extremidade desalocadas. Quando o cliente tenta chamar o procedimento remoto, a biblioteca em tempo de run time do cliente tenta converter novamente o alça totalmente vinculado em um alça parcialmente vinculado. Isso é útil quando o servidor é interrompido e reiniciado usando um ponto de extremidade dinâmico diferente.

 

 




