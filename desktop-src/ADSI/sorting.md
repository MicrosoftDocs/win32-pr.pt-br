---
title: Classificação (ADSI)
description: Um cliente pode solicitar que um servidor Classifique o conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105748337"
---
# <a name="sorting-adsi"></a><span data-ttu-id="133cc-103">Classificação (ADSI)</span><span class="sxs-lookup"><span data-stu-id="133cc-103">Sorting (ADSI)</span></span>

<span data-ttu-id="133cc-104">Um cliente pode solicitar que um servidor Classifique o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="133cc-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="133cc-105">É possível especificar:</span><span class="sxs-lookup"><span data-stu-id="133cc-105">You can specify:</span></span>

-   <span data-ttu-id="133cc-106">Ordem de classificação: a ordem de classificação crescente ou decrescente pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="133cc-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="133cc-107">Atributos de classificação: vários atributos podem ser especificados em uma cadeia de caracteres de classificação.</span><span class="sxs-lookup"><span data-stu-id="133cc-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="133cc-108">Por exemplo, classificar por sobrenome e, em seguida, primeiro nome.</span><span class="sxs-lookup"><span data-stu-id="133cc-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="133cc-109">Ao especificar a ordem de classificação, você deve tentar usar um dos atributos indexados.</span><span class="sxs-lookup"><span data-stu-id="133cc-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="133cc-110">Caso contrário, o servidor deve calcular um conjunto de resultados completo antes de enviá-lo para o cliente.</span><span class="sxs-lookup"><span data-stu-id="133cc-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="133cc-111">Isso é verdadeiro mesmo se você solicitou uma pesquisa paginada e especificou um tamanho de página.</span><span class="sxs-lookup"><span data-stu-id="133cc-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="133cc-112">Nem todos os servidores de diretório dão suporte a várias classificações de atributo ou ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="133cc-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




