---
description: Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitações do OLE Fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a3a1c606a4446129d9e6592c9b352dd0b3e06ae5c77bb378c2430a32cbc568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754246"
---
# <a name="ole-limitations-on-streams"></a>Limitações do OLE Fluxos

Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE Win32. Essas limitações podem afetar as funções do instalador indiretamente por meio de transformaçãos e outros dados que podem ser armazenados no banco de dados como um fluxo.

Há duas limitações relevantes:

-   Os dados binários são armazenados com um nome de índice criado concatenando o nome da tabela e os valores das chaves primárias do registro usando um delimiter de ponto. O OLE limita os nomes de fluxo a 32 caracteres (31 + terminador nulo). Windows O instalador usa um algoritmo de compactação que pode expandir o limite para 62 caracteres, dependendo do caractere. Observe que os caracteres de byte duplo contam como 2.
-   Embora você possa ter vários fluxos abertos ao mesmo tempo, não é possível abrir um fluxo uma segunda vez até que a primeira referência seja fechada. Isso significa que você não pode selecionar o mesmo fluxo de dados binário para ser aberto em vários registros simultaneamente. As tentativas de ler os dados binários do segundo registro falham. Além disso, não é possível renomear as chaves primárias de um registro enquanto um fluxo de dados binário nesse registro está aberto.

 

 



