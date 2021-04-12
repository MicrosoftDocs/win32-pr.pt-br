---
title: Processando reservas
description: As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no repositório de reserva persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104366887"
---
# <a name="processing-reservations"></a><span data-ttu-id="4fe92-103">Processando reservas</span><span class="sxs-lookup"><span data-stu-id="4fe92-103">Processing Reservations</span></span>

<span data-ttu-id="4fe92-104">As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no repositório de reserva persistente.</span><span class="sxs-lookup"><span data-stu-id="4fe92-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="4fe92-105">A raiz do namespace da URL para HTTP pertence ao administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="4fe92-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="4fe92-106">Para todos os valores de porta e host, as duas reservas a seguir são sempre presumidas na raiz do namespace **relativeUri** .</span><span class="sxs-lookup"><span data-stu-id="4fe92-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="4fe92-107">Namespace reservado</span><span class="sxs-lookup"><span data-stu-id="4fe92-107">Namespace reserved</span></span>                 | <span data-ttu-id="4fe92-108">Reservado para</span><span class="sxs-lookup"><span data-stu-id="4fe92-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="4fe92-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="4fe92-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="4fe92-110">Administrador LocalSystem</span><span class="sxs-lookup"><span data-stu-id="4fe92-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="4fe92-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="4fe92-111">https://<host>:<port>/</span></span> | <span data-ttu-id="4fe92-112">Administrador LocalSystem</span><span class="sxs-lookup"><span data-stu-id="4fe92-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="4fe92-113">Essas reservas implícitas não podem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="4fe92-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="4fe92-114">No entanto, é possível delegar reservas de raiz explícitas a outros usuários.</span><span class="sxs-lookup"><span data-stu-id="4fe92-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="4fe92-115">As reservas, como a seguir, criaria tais delegações:</span><span class="sxs-lookup"><span data-stu-id="4fe92-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="4fe92-116">Namespace reservado</span><span class="sxs-lookup"><span data-stu-id="4fe92-116">Namespace reserved</span></span>        | <span data-ttu-id="4fe92-117">Reservado para</span><span class="sxs-lookup"><span data-stu-id="4fe92-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="4fe92-118">UserA, UserC</span><span class="sxs-lookup"><span data-stu-id="4fe92-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="4fe92-119">UserB</span><span class="sxs-lookup"><span data-stu-id="4fe92-119">UserB</span></span>        |



 

<span data-ttu-id="4fe92-120">Se essas reservas delegadas forem removidas pelo administrador do sistema, a propriedade do namespace será revertida para a Reserva implícita para os valores de host e porta correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4fe92-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




