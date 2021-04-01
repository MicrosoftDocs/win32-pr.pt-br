---
description: A LSA armazena informações de política de segurança local em um conjunto de objetos. Seu aplicativo pode consultar ou editar a política de segurança local acessando esses objetos.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objetos de política LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921842"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="89b94-104">Objetos de política LSA</span><span class="sxs-lookup"><span data-stu-id="89b94-104">LSA Policy Objects</span></span>

<span data-ttu-id="89b94-105">A LSA armazena informações de política de segurança local em um conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="89b94-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="89b94-106">Seu aplicativo pode consultar ou editar a política de segurança local acessando esses objetos.</span><span class="sxs-lookup"><span data-stu-id="89b94-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="89b94-107">O conjunto consiste nos quatro objetos a seguir:</span><span class="sxs-lookup"><span data-stu-id="89b94-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="89b94-108">A [política](policy-object.md) contém informações de política global.</span><span class="sxs-lookup"><span data-stu-id="89b94-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="89b94-109">[TrustedDomain](trusteddomain-object.md) contém informações sobre um domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="89b94-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="89b94-110">[Conta](account-object.md) contém informações sobre um usuário, grupo ou conta de grupo local.</span><span class="sxs-lookup"><span data-stu-id="89b94-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="89b94-111">[Os dados privados](private-data-object.md) contêm informações protegidas, como senhas de conta de servidor.</span><span class="sxs-lookup"><span data-stu-id="89b94-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="89b94-112">Essas informações são armazenadas como cadeias de caracteres criptografadas.</span><span class="sxs-lookup"><span data-stu-id="89b94-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="89b94-113">Para obter mais informações sobre como usar as funções de política LSA para gerenciar as informações armazenadas nesses objetos, consulte [usando a política LSA](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="89b94-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



