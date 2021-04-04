---
title: Destinos
description: Um destino na tabela de roteamento é uma entrada de rede representada por um endereço de rede e uma máscara de rede.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822699"
---
# <a name="destinations"></a><span data-ttu-id="73118-103">Destinos</span><span class="sxs-lookup"><span data-stu-id="73118-103">Destinations</span></span>

<span data-ttu-id="73118-104">Um destino na tabela de roteamento é uma entrada de rede representada por um endereço de rede e uma máscara de rede.</span><span class="sxs-lookup"><span data-stu-id="73118-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="73118-105">Uma entrada de destino na tabela de roteamento inclui:</span><span class="sxs-lookup"><span data-stu-id="73118-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="73118-106">O endereço, expresso como um endereço de rede e uma máscara de rede.</span><span class="sxs-lookup"><span data-stu-id="73118-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="73118-107">Uma lista de rotas para o destino.</span><span class="sxs-lookup"><span data-stu-id="73118-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="73118-108">Uma lista de Slots de ponteiro opacos.</span><span class="sxs-lookup"><span data-stu-id="73118-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="73118-109">As exibições nas quais esse destino é válido.</span><span class="sxs-lookup"><span data-stu-id="73118-109">The views in which this destination is valid.</span></span> <span data-ttu-id="73118-110">O destino contém uma estrutura para cada exibição que contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="73118-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="73118-111">Um identificador para a exibição.</span><span class="sxs-lookup"><span data-stu-id="73118-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="73118-112">Um ponteiro para a melhor rota para o destino nesta exibição.</span><span class="sxs-lookup"><span data-stu-id="73118-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="73118-113">O proprietário da melhor rota nessa exibição.</span><span class="sxs-lookup"><span data-stu-id="73118-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="73118-114">Sinalizadores associados à melhor rota nesta exibição.</span><span class="sxs-lookup"><span data-stu-id="73118-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="73118-115">Identificador para qualquer rota que esteja em um estado suspenso nesta exibição.</span><span class="sxs-lookup"><span data-stu-id="73118-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




