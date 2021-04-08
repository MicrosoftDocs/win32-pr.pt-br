---
title: Funções de informações do roteador
description: Use as funções a seguir para manipular blocos e cabeçalhos de informações do roteador. Um cabeçalho de informações é composto de metadados privados e blocos de informações. Os blocos de informações são matrizes de estruturas de informações de vários tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004787"
---
# <a name="router-information-functions"></a>Funções de informações do roteador

Use as funções a seguir para manipular blocos e cabeçalhos de informações do roteador. Um cabeçalho de informações é composto de metadados privados e blocos de informações. Os blocos de informações são matrizes de [estruturas de informações](router-information-structures.md) de vários [tipos](router-information-enumerations.md).

As seguintes funções manipulam os cabeçalhos de informações:

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

As seguintes funções manipulam blocos de informações dentro de um cabeçalho de informações:

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

Muitas das [funções de administração e configuração do roteador](understanding-mprinfo-functions-and-information-headers.md) usam cabeçalhos de informações.

 

 




