---
description: A partir do Windows 8, a Microsoft começou a distribuir os provedores que permitem o compartilhamento seguro de mensagens e segredos criptografados entre computadores.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Provedores de proteção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921415"
---
# <a name="protection-providers"></a><span data-ttu-id="7b621-103">Provedores de proteção</span><span class="sxs-lookup"><span data-stu-id="7b621-103">Protection Providers</span></span>

<span data-ttu-id="7b621-104">A partir do Windows 8, a Microsoft começou a distribuir os provedores que permitem o compartilhamento seguro de mensagens e segredos criptografados entre computadores.</span><span class="sxs-lookup"><span data-stu-id="7b621-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="7b621-105">Atualmente, há dois provedores de proteção de chave.</span><span class="sxs-lookup"><span data-stu-id="7b621-105">There are currently two key protection providers.</span></span> <span data-ttu-id="7b621-106">O provedor de proteção de chave da Microsoft permite que você proteja o conteúdo a um grupo em uma floresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b621-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="7b621-107">O provedor de proteção de chave do cliente da Microsoft permite que você proteja o conteúdo para um conjunto de credenciais da Web.</span><span class="sxs-lookup"><span data-stu-id="7b621-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="7b621-108">O protetor correto a ser usado é escolhido automaticamente para você quando a função [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analisa a cadeia de caracteres de regra do descritor de proteção que você fornece como entrada.</span><span class="sxs-lookup"><span data-stu-id="7b621-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="7b621-109">O provedor de proteção de chave da Microsoft é escolhido para cadeias de caracteres de regra que começam com SID, SDDL e LOCAL.</span><span class="sxs-lookup"><span data-stu-id="7b621-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="7b621-110">O provedor de proteção de chave do cliente da Microsoft analisa cadeias de caracteres de regra que começam com webcredentials.</span><span class="sxs-lookup"><span data-stu-id="7b621-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="7b621-111">Para obter mais informações sobre cadeias de caracteres de regra, consulte [descritores de proteção](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7b621-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="7b621-112">Os provedores personalizados não são permitidos no momento. [DPAPI CNG](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="7b621-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b621-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b621-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b621-114">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="7b621-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="7b621-115">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7b621-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="7b621-116">Descritores de proteção</span><span class="sxs-lookup"><span data-stu-id="7b621-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



