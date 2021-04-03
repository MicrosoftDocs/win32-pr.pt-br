---
description: Explica as interações entre o Winlogon e os provedores de rede.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interação com provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829758"
---
# <a name="interaction-with-network-providers"></a><span data-ttu-id="0a443-103">Interação com provedores de rede</span><span class="sxs-lookup"><span data-stu-id="0a443-103">Interaction with Network Providers</span></span>

<span data-ttu-id="0a443-104">Você pode configurar um sistema para dar suporte a zero ou mais provedores de rede.</span><span class="sxs-lookup"><span data-stu-id="0a443-104">You can configure a system to support zero or more network providers.</span></span> <span data-ttu-id="0a443-105">Cada um desses provedores de rede pode especificar que ele requer processamento de autenticação interativa especial.</span><span class="sxs-lookup"><span data-stu-id="0a443-105">Each of these network providers can specify that it requires special interactive authentication processing.</span></span> <span data-ttu-id="0a443-106">Esse recurso permite que as redes instaladas coletem informações de identificação e de autenticação específicas para cada rede, mas, ainda assim, permitem que elas as coletem durante o logon normal e sob a proteção segura do [*contexto*](../secgloss/c-gly.md) e da área de trabalho [*do Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0a443-106">This capability allows installed networks to collect identification and authentication information specific to each network, yet allows them to collect it during normal logon and under the secure umbrella of [*Winlogon's*](../secgloss/w-gly.md) [*context*](../secgloss/c-gly.md) and desktop.</span></span>

<span data-ttu-id="0a443-107">O Winlogon chama provedores de rede em várias circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="0a443-107">Winlogon calls network providers under a number of circumstances.</span></span> <span data-ttu-id="0a443-108">Após um logon bem-sucedido, o Winlogon chama os provedores de rede para que eles possam coletar [*credenciais*](../secgloss/c-gly.md) e autenticar o usuário para sua rede.</span><span class="sxs-lookup"><span data-stu-id="0a443-108">Following a successful logon, Winlogon calls network providers so they can collect [*credentials*](../secgloss/c-gly.md) and authenticate the user for their network.</span></span> <span data-ttu-id="0a443-109">O Winlogon também chama provedores de rede quando os usuários alteram suas senhas.</span><span class="sxs-lookup"><span data-stu-id="0a443-109">Winlogon also calls network providers when users change their passwords.</span></span> <span data-ttu-id="0a443-110">Isso permite que cada usuário mantenha uma única senha para uso em todas as redes.</span><span class="sxs-lookup"><span data-stu-id="0a443-110">This lets each user maintain a single password for use on all networks.</span></span>

<span data-ttu-id="0a443-111">A estrutura de [**\_ informações de \_ notificação \_ do WLX MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) é usada para fornecer informações de identificação e autenticação nas funções de Gina relevantes.</span><span class="sxs-lookup"><span data-stu-id="0a443-111">The [**WLX\_MPR\_NOTIFY\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) structure is used to provide identification and authentication information in the relevant GINA functions.</span></span> <span data-ttu-id="0a443-112">Essa estrutura inclui os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a443-112">This structure includes the following members.</span></span>



| <span data-ttu-id="0a443-113">Membro</span><span class="sxs-lookup"><span data-stu-id="0a443-113">Member</span></span>             | <span data-ttu-id="0a443-114">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="0a443-114">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a443-115">**pszUserName**</span><span class="sxs-lookup"><span data-stu-id="0a443-115">**pszUserName**</span></span>    | <span data-ttu-id="0a443-116">O nome da conta do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="0a443-116">The account name of the logged-on user.</span></span>                                                                                                                                                      |
| <span data-ttu-id="0a443-117">**pszDomain**</span><span class="sxs-lookup"><span data-stu-id="0a443-117">**pszDomain**</span></span>      | <span data-ttu-id="0a443-118">O nome de domínio do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="0a443-118">The domain name of the logged-on user.</span></span> <span data-ttu-id="0a443-119">Nem todos os modelos de autenticação têm um conceito de domínio (ou seu equivalente), portanto, esse membro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0a443-119">Not all authentication models have a domain concept (or its equivalent), so this member can be **NULL**.</span></span>                                              |
| <span data-ttu-id="0a443-120">**pszPassword**</span><span class="sxs-lookup"><span data-stu-id="0a443-120">**pszPassword**</span></span>    | <span data-ttu-id="0a443-121">Quando o usuário forneceu uma senha de texto sem formatação durante a autenticação, fornecê-la aqui permite que outros provedores de rede usem a mesma senha (para obter logon único) sem avisar o usuário.</span><span class="sxs-lookup"><span data-stu-id="0a443-121">When the user gave a plaintext password during authentication, providing it here lets other network providers use the same password (to achieve single logon) without prompting the user.</span></span>    |
| <span data-ttu-id="0a443-122">**pszOldPassword**</span><span class="sxs-lookup"><span data-stu-id="0a443-122">**pszOldPassword**</span></span> | <span data-ttu-id="0a443-123">Após uma alteração de senha, fornecendo a senha original aqui e a nova senha no membro **pszPassword** , permite que os provedores de rede atualizem suas senhas sem avisar o usuário.</span><span class="sxs-lookup"><span data-stu-id="0a443-123">After a password change, providing the original password here and the new password in the **pszPassword** member, lets network providers upgrade their passwords without prompting the user.</span></span> |



 

<span data-ttu-id="0a443-124">Uma [*Gina*](../secgloss/g-gly.md) não precisa fornecer essas informações aos provedores de rede.</span><span class="sxs-lookup"><span data-stu-id="0a443-124">A [*GINA*](../secgloss/g-gly.md) does not have to provide this information to network providers.</span></span> <span data-ttu-id="0a443-125">Se um ponteiro **NULL** for passado em vez de um ponteiro de estrutura válido, os provedores de rede solicitarão as informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0a443-125">If a **NULL** pointer is passed instead of a valid structure pointer, the network providers will prompt the user for information.</span></span>

 

 
