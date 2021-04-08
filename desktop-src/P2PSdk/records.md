---
description: Os registros são uma maneira de se comunicar entre os nós em um grafo ou membros de um grupo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922243"
---
# <a name="records"></a><span data-ttu-id="5d6e7-103">Registros</span><span class="sxs-lookup"><span data-stu-id="5d6e7-103">Records</span></span>

<span data-ttu-id="5d6e7-104">Os registros são uma maneira de se comunicar entre os nós em um grafo ou membros de um grupo.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="5d6e7-105">Um registro consiste nas duas partes a seguir:</span><span class="sxs-lookup"><span data-stu-id="5d6e7-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="5d6e7-106">Cabeçalho de registro</span><span class="sxs-lookup"><span data-stu-id="5d6e7-106">Record header</span></span>
-   <span data-ttu-id="5d6e7-107">Conteúdo de dados opaco específico</span><span class="sxs-lookup"><span data-stu-id="5d6e7-107">Specific opaque data content</span></span>

<span data-ttu-id="5d6e7-108">O cabeçalho contém informações sobre o registro, incluindo a versão, o criador e o tipo de dados que estão sendo publicados.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="5d6e7-109">O cabeçalho também contém um campo atributos XML que permite que os aplicativos adicionem atributos de nome-valor que descrevem os dados e pesquisem com eficiência o banco de dados de registro para obter registros específicos que foram publicados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="5d6e7-110">O conteúdo são os dados definidos pelo aplicativo e é opaco para a infraestrutura do par.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="5d6e7-111">Quando um registro é publicado, ele (cabeçalho e dados) é inundado em todo o grafo ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="5d6e7-112">Os pares sincronizados recebem esses dados e os armazenam em um banco de dados local.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="5d6e7-113">Os pares não sincronizados e offline recebem os dados na próxima vez que se conectarem e sincronizarem com o grafo ou o grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="5d6e7-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="5d6e7-114">Para obter informações sobre como trabalhar com registros, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5d6e7-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="5d6e7-115">Dependências de registro</span><span class="sxs-lookup"><span data-stu-id="5d6e7-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="5d6e7-116">Gerenciamento de registros</span><span class="sxs-lookup"><span data-stu-id="5d6e7-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="5d6e7-117">Esquema de atributo de registro</span><span class="sxs-lookup"><span data-stu-id="5d6e7-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="5d6e7-118">Gravar formato de consulta de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5d6e7-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 



