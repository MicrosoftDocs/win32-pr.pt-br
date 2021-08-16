---
title: Funções de informações do roteador
description: Use as funções a seguir para manipular blocos e cabeçalhos de informações do roteador. Um cabeçalho de informações é composto de metadados privados e blocos de informações. Os blocos de informações são matrizes de estruturas de informações de vários tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029b36ef862f11c58492fd8ec9c7c6f292797c2e35e75592f385e18d6d0e1a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788011"
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

 

 




