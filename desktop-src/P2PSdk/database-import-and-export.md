---
description: Ao usar o gráfico de pares ou as infraestruturas de agrupamento de pares, as informações (registros) que os colegas publicam em um grafo ou grupo são armazenadas como um banco de dados em cada computador de mesmo nível.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importação e exportação de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc047e6f58c7aeab07f6d13f8f7364f3f2f1191e50320513bc153e34c4c042c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979056"
---
# <a name="database-import-and-export"></a>Importação e exportação de banco de dados

Ao usar o gráfico de pares ou as infraestruturas de agrupamento de pares, as informações (registros) que os colegas publicam em um grafo ou grupo são armazenadas como um banco de dados em cada computador de mesmo nível. Para migrar um aplicativo de um computador para outro, você pode exportar um gráfico de pares ou um banco de dados de agrupamento de pares de um computador e, em seguida, importá-lo para outro.

A lista a seguir identifica informações importantes sobre como trabalhar com bancos de dados:

-   Você só pode importar um banco de dados que tenha o mesmo grafo e ID de mesmo nível.
-   Você não poderá chamar as funções de importação e exportação se [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)ou [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) tiverem sido chamados.

A **infraestrutura de grafo de pares** usa as seguintes chamadas para importar e exportar um banco de dados de registro:

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

A **infraestrutura de agrupamento de pares** usa as seguintes chamadas para importar e exportar um banco de dados de registro:

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



