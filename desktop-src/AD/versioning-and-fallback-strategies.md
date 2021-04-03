---
title: Estratégias de controle de versão e fallback
description: Quando um aplicativo detecta uma atualização parcial usando uma das técnicas anteriores ou lê um conjunto de objetos cuja data de efetivação ainda não foi atingida, o aplicativo deve lidar com a situação normalmente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de estratégias de controle de versão e fallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822249"
---
# <a name="versioning-and-fallback-strategies"></a>Estratégias de controle de versão e fallback

Quando um aplicativo detecta uma atualização parcial usando uma das técnicas anteriores ou lê um conjunto de objetos cuja data de efetivação ainda não foi atingida, o aplicativo deve lidar com a situação normalmente. Para alguns aplicativos, a resposta normal é "retorne" para uma versão anterior dos objetos em questão. Active Directory Domain Services não fornecem um recurso de controle de versão – os aplicativos que desejam esse recurso devem fornecê-lo por conta própria. As abordagens para controle de versão incluem manter os valores "última boa conhecida" armazenados em cache localmente e armazenar vários conjuntos de objetos no diretório, por exemplo, nos contêineres "antigo", "atual" e "novo". Muitos outros esquemas são possíveis.

As implementações devem tomar cuidado para evitar consequências indesejadas. Uma versão anterior dos objetos deve ser usada somente quando uma atualização parcial é detectada ou os novos objetos ainda não estão "efetivos". Fazer fallback porque algo no aplicativo "não funciona" pode burlar a intenção de um administrador. Por exemplo, dois computadores que antes podiam se comunicar podem não conseguir fazê-lo devido a uma alteração na diretiva de protocolo IPsec. Se isso for intencional por parte do administrador, os sistemas afetados não devem retornar à política que permitia a comunicação, pois isso seria uma violação de segurança.

 

 




