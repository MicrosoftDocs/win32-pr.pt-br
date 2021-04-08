---
description: 'Saiba mais sobre: indexação na tabela'
title: Indexação na tabela
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010615"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="5a92b-103">Indexação na tabela</span><span class="sxs-lookup"><span data-stu-id="5a92b-103">Indexing in the Table</span></span>


<span data-ttu-id="5a92b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a92b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="5a92b-105">Indexação na tabela</span><span class="sxs-lookup"><span data-stu-id="5a92b-105">Indexing in the Table</span></span>

<span data-ttu-id="5a92b-106">Um índice é um conjunto de colunas de chave que definem uma ordenação persistente de registros em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5a92b-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="5a92b-107">Registros são entradas de índice no índice primário.</span><span class="sxs-lookup"><span data-stu-id="5a92b-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="5a92b-108">Um índice primário e vários índices secundários podem ser definidos para criar diferentes ordens de dados na tabela.</span><span class="sxs-lookup"><span data-stu-id="5a92b-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="5a92b-109">Embora vários índices possam ser definidos, os registros são fisicamente armazenados em árvores B + na ordem especificada pelo índice primário.</span><span class="sxs-lookup"><span data-stu-id="5a92b-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="5a92b-110">O índice primário é sempre um índice clusterizado e também deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5a92b-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="5a92b-111">O índice primário deve ser declarado antes da primeira atualização da tabela para preservar a ordenação do índice.</span><span class="sxs-lookup"><span data-stu-id="5a92b-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="5a92b-112">Quando nenhum índice primário é definido pelo aplicativo, os dados são armazenados na ordem em que os registros são adicionados à tabela.</span><span class="sxs-lookup"><span data-stu-id="5a92b-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="5a92b-113">Esse índice especial é conhecido como um índice sequencial.</span><span class="sxs-lookup"><span data-stu-id="5a92b-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="5a92b-114">Separe as árvores B + usadas para ordenar registros de acordo com o índice secundário.</span><span class="sxs-lookup"><span data-stu-id="5a92b-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="5a92b-115">As entradas de índice no índice secundário contêm ponteiros para os dados armazenados de acordo com o índice primário.</span><span class="sxs-lookup"><span data-stu-id="5a92b-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="5a92b-116">As entradas de índice para registros no índice primário devem ser exclusivas porque o índice secundário aponta para o registro usando a chave primária do registro.</span><span class="sxs-lookup"><span data-stu-id="5a92b-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="5a92b-117">Os índices secundários podem ou não ter uma restrição de exclusividade.</span><span class="sxs-lookup"><span data-stu-id="5a92b-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="5a92b-118">Para obter mais informações, consulte o tópico [visão geral do banco de dados](./database-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="5a92b-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
