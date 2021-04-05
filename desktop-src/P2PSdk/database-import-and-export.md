---
description: Ao usar o gráfico de pares ou as infraestruturas de agrupamento de pares, as informações (registros) que os colegas publicam em um grafo ou grupo são armazenadas como um banco de dados em cada computador de mesmo nível.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importação e exportação de banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921769"
---
# <a name="database-import-and-export"></a><span data-ttu-id="90b14-103">Importação e exportação de banco de dados</span><span class="sxs-lookup"><span data-stu-id="90b14-103">Database Import and Export</span></span>

<span data-ttu-id="90b14-104">Ao usar o gráfico de pares ou as infraestruturas de agrupamento de pares, as informações (registros) que os colegas publicam em um grafo ou grupo são armazenadas como um banco de dados em cada computador de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="90b14-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="90b14-105">Para migrar um aplicativo de um computador para outro, você pode exportar um gráfico de pares ou um banco de dados de agrupamento de pares de um computador e, em seguida, importá-lo para outro.</span><span class="sxs-lookup"><span data-stu-id="90b14-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="90b14-106">A lista a seguir identifica informações importantes sobre como trabalhar com bancos de dados:</span><span class="sxs-lookup"><span data-stu-id="90b14-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="90b14-107">Você só pode importar um banco de dados que tenha o mesmo grafo e ID de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="90b14-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="90b14-108">Você não poderá chamar as funções de importação e exportação se [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)ou [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) tiverem sido chamados.</span><span class="sxs-lookup"><span data-stu-id="90b14-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="90b14-109">A **infraestrutura de grafo de pares** usa as seguintes chamadas para importar e exportar um banco de dados de registro:</span><span class="sxs-lookup"><span data-stu-id="90b14-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="90b14-110">**PeerGraphExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="90b14-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="90b14-111">**PeerGraphImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="90b14-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="90b14-112">A **infraestrutura de agrupamento de pares** usa as seguintes chamadas para importar e exportar um banco de dados de registro:</span><span class="sxs-lookup"><span data-stu-id="90b14-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="90b14-113">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="90b14-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="90b14-114">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="90b14-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



