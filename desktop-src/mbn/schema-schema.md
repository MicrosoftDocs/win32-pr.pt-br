---
description: Define um perfil de banda larga móvel.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Referência de esquema de perfil de banda larga móvel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783217"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="3db96-103">Referência de esquema de perfil de banda larga móvel</span><span class="sxs-lookup"><span data-stu-id="3db96-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="3db96-104">O esquema de perfil de banda larga móvel define um perfil de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="3db96-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="3db96-105">Os perfis armazenam parâmetros de configuração de rede e de usuário relacionados à conexão de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="3db96-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="3db96-106">Eles também armazenam as preferências do usuário para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="3db96-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="3db96-107">O elemento raiz de um perfil de banda larga móvel é o elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3db96-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="3db96-108">Cada perfil tem exatamente um elemento raiz.</span><span class="sxs-lookup"><span data-stu-id="3db96-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="3db96-109">Todos os elementos do esquema de perfil de banda larga móvel usados pelo Windows 7 estão no namespace `https://www.microsoft.com/networking/WWAN/profile/v1` e os elementos usados pelo Windows 8 estão no namespace `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="3db96-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="3db96-110">O esquema de perfil de banda larga móvel impõe estritamente a ordem dos nós.</span><span class="sxs-lookup"><span data-stu-id="3db96-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="3db96-111">Os nós especificados em um perfil devem aderir ao **esquema de perfil de banda larga móvel** e aparecer na ordem prescrita na definição do esquema.</span><span class="sxs-lookup"><span data-stu-id="3db96-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="3db96-112">Por exemplo, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) deve ser especificado imediatamente após [**accessstring**](schema-accessstring-contexttype-element.md).</span><span class="sxs-lookup"><span data-stu-id="3db96-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="3db96-113">Esquema de perfil de banda larga móvel v1</span><span class="sxs-lookup"><span data-stu-id="3db96-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="3db96-114">Esquema de perfil de banda larga móvel v2</span><span class="sxs-lookup"><span data-stu-id="3db96-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="3db96-115">Esquema de perfil de banda larga móvel v3</span><span class="sxs-lookup"><span data-stu-id="3db96-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="3db96-116">[Esquema de perfil de banda larga móvel v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3db96-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
