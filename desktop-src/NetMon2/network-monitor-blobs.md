---
description: O BLOB (objeto binário grande) Monitor de Rede é uma estrutura de dados genérica que contém informações de configuração e local de NICs (placas de interface de rede).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BLOBs de Monitor de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800106"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="4e979-103">BLOBs de Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="4e979-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="4e979-104">O BLOB (objeto binário grande) Monitor de Rede é uma estrutura de dados genérica que contém informações de configuração e local de NICs (placas de interface de rede).</span><span class="sxs-lookup"><span data-stu-id="4e979-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="4e979-105">Use BLOBs para representar NICs e para filtrar entradas em uma lista de NICs.</span><span class="sxs-lookup"><span data-stu-id="4e979-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="4e979-106">Os BLOBs também podem conter dados específicos do aplicativo sem afetar os outros dados que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="4e979-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="4e979-107">A implementação de BLOB é opaca para todos os níveis que devem acessar BLOBs com APIs de BLOB.</span><span class="sxs-lookup"><span data-stu-id="4e979-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="4e979-108">Estrutura do BLOB</span><span class="sxs-lookup"><span data-stu-id="4e979-108">BLOB Structure</span></span>

<span data-ttu-id="4e979-109">Um BLOB pode ser considerado uma árvore hierárquica usada para designar cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e979-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="4e979-110">Esta árvore tem três camadas: proprietário, categoria e marca.</span><span class="sxs-lookup"><span data-stu-id="4e979-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="4e979-111">Owner é uma cadeia de caracteres que indica, em geral, que lê uma entrada.</span><span class="sxs-lookup"><span data-stu-id="4e979-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="4e979-112">A categoria também é uma cadeia de caracteres, que designa um agrupamento funcional geral de marcas sob o proprietário.</span><span class="sxs-lookup"><span data-stu-id="4e979-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="4e979-113">A marca é o nome real da entrada.</span><span class="sxs-lookup"><span data-stu-id="4e979-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="4e979-114">As características estruturais dos BLOBs incluem:</span><span class="sxs-lookup"><span data-stu-id="4e979-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="4e979-115">Os auxiliares de BLOB em um processo são protegidos uns dos outros por um mutex embutido em cada BLOB.</span><span class="sxs-lookup"><span data-stu-id="4e979-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="4e979-116">Cada BLOB tem um número de versão interno para que os auxiliares possam lidar com formulários de BLOB presentes e futuros.</span><span class="sxs-lookup"><span data-stu-id="4e979-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="4e979-117">Poderão ocorrer conflitos de versão se você enviar um BLOB para outro computador por meio de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4e979-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="4e979-118">O BLOB em si é um ponteiro para void.</span><span class="sxs-lookup"><span data-stu-id="4e979-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="4e979-119">Lembre-se de que os aplicativos devem alocar BLOBs com o modificador **const** para evitar alterar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4e979-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="4e979-120">Cada um dos designadores, bem como seus valores, são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e979-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="4e979-121">Lembre-se de que as cadeias de caracteres retornadas por funções **GetString** são, na verdade, ponteiros para o blob e não devem ser alteradas.</span><span class="sxs-lookup"><span data-stu-id="4e979-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="4e979-122">Por esse motivo, essas cadeias de caracteres devem ser especificadas como **const char** _ \_ PX \* para impedir que os aplicativos as alterem acidentalmente.</span><span class="sxs-lookup"><span data-stu-id="4e979-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="4e979-123">Em geral, todos os parâmetros com o designador **const** incentivam o chamador a evitar a alteração dos valores em vez de proibir as funções auxiliares de alterá-las.</span><span class="sxs-lookup"><span data-stu-id="4e979-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="4e979-124">Na verdade, as funções auxiliares geralmente alterarão esses valores.</span><span class="sxs-lookup"><span data-stu-id="4e979-124">In fact, the helper functions will usually change those values.</span></span>

 

 



