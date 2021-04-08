---
description: A API do Gerenciador de identidades do par permite que você crie, enumere e manipule identidades pares em um aplicativo par.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Sobre o Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828417"
---
# <a name="about-identity-manager"></a><span data-ttu-id="edb46-103">Sobre o Identity Manager</span><span class="sxs-lookup"><span data-stu-id="edb46-103">About Identity Manager</span></span>

<span data-ttu-id="edb46-104">A API do Gerenciador de identidades do par permite que você crie, enumere e manipule identidades pares em um aplicativo par.</span><span class="sxs-lookup"><span data-stu-id="edb46-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="edb46-105">Você pode usar as identidades de par criadas usando essa API como entrada para as APIs do provedor de namespace par e PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="edb46-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="edb46-106">Práticas recomendadas do Gerenciador de identidade do par</span><span class="sxs-lookup"><span data-stu-id="edb46-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="edb46-107">Cada usuário deve ter algumas identidades pares que podem usar para as atividades do par.</span><span class="sxs-lookup"><span data-stu-id="edb46-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="edb46-108">Por exemplo, um usuário pode ter duas identidades pares para trabalho e lazer.</span><span class="sxs-lookup"><span data-stu-id="edb46-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="edb46-109">Um aplicativo de par bem projetado permite que um usuário selecione uma identidade de par a ser usada.</span><span class="sxs-lookup"><span data-stu-id="edb46-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="edb46-110">Um usuário poderá criar uma nova identidade de par se nenhuma identidade de par existente for apropriada para uso com um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edb46-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="edb46-111">Um aplicativo par bem projetado também controla o número de identidades que ele cria.</span><span class="sxs-lookup"><span data-stu-id="edb46-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="edb46-112">Se um aplicativo criar uma identidade de par temporária, o aplicativo deverá excluir a identidade do par quando a identidade não for necessária.</span><span class="sxs-lookup"><span data-stu-id="edb46-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="edb46-113">Se um aplicativo não executar essa manutenção, o Gerenciador de identidade do par poderá não ser capaz de criar identidades pares até que algumas identidades de mesmo nível sejam removidas.</span><span class="sxs-lookup"><span data-stu-id="edb46-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



