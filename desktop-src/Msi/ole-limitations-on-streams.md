---
description: Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitações de OLE em fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164829"
---
# <a name="ole-limitations-on-streams"></a>Limitações de OLE em fluxos

Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32. Essas limitações podem afetar as funções do instalador indiretamente por meio de transformações e outros dados que podem ser armazenados no banco de dado como um fluxo.

Há duas limitações relevantes:

-   Os dados binários são armazenados com um nome de índice criado concatenando o nome da tabela e os valores das chaves primárias do registro usando um delimitador de período. O OLE limita os nomes de fluxo a 32 caracteres (31 + terminador nulo). Windows Installer usa um algoritmo de compactação que pode expandir o limite para 62 caracteres, dependendo do caractere. Observe que os caracteres de byte duplo contam como 2.
-   Embora você possa ter vários fluxos abertos ao mesmo tempo, não é possível abrir um fluxo uma segunda vez até que a primeira referência seja fechada. Isso significa que você não pode selecionar o mesmo fluxo de dados binários a ser aberto em vários registros simultaneamente. Falha nas tentativas de ler os dados binários do segundo registro. Além disso, você não pode renomear as chaves primárias de um registro enquanto um fluxo de dados binários nesse registro estiver aberto.

 

 



