---
description: A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Sobre a API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171686"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="97639-103">Sobre a API Wi-Fi nativa</span><span class="sxs-lookup"><span data-stu-id="97639-103">About the Native Wifi API</span></span>

<span data-ttu-id="97639-104">A API Wi-Fi nativa contém funções, estruturas e enumerações que dão suporte à conectividade de rede sem fio e ao gerenciamento de perfil sem fio.</span><span class="sxs-lookup"><span data-stu-id="97639-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="97639-105">A API pode ser usada para redes de infraestrutura e ad hoc.</span><span class="sxs-lookup"><span data-stu-id="97639-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="97639-106">A API ad hoc sem fio é uma interface simplificada orientada a objeto para criar, gerenciar e usar redes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="97639-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="97639-107">O modo ad hoc pode não estar disponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="97639-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="97639-108">A partir do Windows 8.1 e do Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="97639-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="97639-109">A implementação da API ad hoc usa a API Wi-Fi nativa.</span><span class="sxs-lookup"><span data-stu-id="97639-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="97639-110">Isso significa que as chamadas de API ad hoc podem disparar notificações Wi-Fi nativas e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="97639-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="97639-111">Misturar chamadas nativas à API WiFi e chamadas de API ad hoc sem fio não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="97639-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="97639-112">Os desenvolvedores devem escolher uma abordagem de programação antes de criar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97639-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="97639-113">Se seu aplicativo usar ou gerenciar redes de infraestrutura, você deverá usar a API Wi-Fi nativa.</span><span class="sxs-lookup"><span data-stu-id="97639-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="97639-114">Se seu aplicativo exigir a funcionalidade de gerenciamento de perfil, você deverá usar a API Wi-Fi nativa.</span><span class="sxs-lookup"><span data-stu-id="97639-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="97639-115">Caso contrário, você deve usar a API ad hoc sem fio.</span><span class="sxs-lookup"><span data-stu-id="97639-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97639-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97639-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97639-117">Sobre WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="97639-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="97639-118">Suporte nativo à API WiFi no Windows XP</span><span class="sxs-lookup"><span data-stu-id="97639-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="97639-119">Permissões nativas da API WiFi</span><span class="sxs-lookup"><span data-stu-id="97639-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="97639-120">Sobre a API ad hoc sem fio</span><span class="sxs-lookup"><span data-stu-id="97639-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="97639-121">Baixe o SDK do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97639-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



