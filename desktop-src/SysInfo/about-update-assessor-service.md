---
description: O tópico a seguir descreve como a API da plataforma de avaliação WaaS (Windows as a Service) funciona.
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Sobre a plataforma de avaliação do WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756129"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="23809-103">Sobre a plataforma de avaliação do WaaS</span><span class="sxs-lookup"><span data-stu-id="23809-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="23809-104">O tópico a seguir descreve como a API da plataforma de avaliação WaaS (Windows as a Service) funciona.</span><span class="sxs-lookup"><span data-stu-id="23809-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="23809-105">A API de avaliação do WaaS oferece ao chamador as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="23809-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="23809-106">Se um dispositivo estiver nas atualizações mais recentes da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="23809-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="23809-107">Se o dispositivo atingiu o fim do suporte.</span><span class="sxs-lookup"><span data-stu-id="23809-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="23809-108">Os tempos de liberação para as atualizações mais recentes aplicáveis para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23809-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="23809-109">Uma avaliação do motivo pelo qual um dispositivo não está atualizado e o impacto potencial que ele pode ter no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23809-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="23809-110">A plataforma de avaliação do WaaS usa o modelo de API COM e é executada automaticamente pelo menos uma vez por dia.</span><span class="sxs-lookup"><span data-stu-id="23809-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="23809-111">Esse ciclo captura as informações de versão aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="23809-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="23809-112">Durante o período em cache, as avaliações são feitas em relação às informações de versão armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="23809-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="23809-113">Se uma chamada for feita fora da janela de expiração do cache, uma nova chamada e uma avaliação serão feitas, armazenadas em cache e retornadas.</span><span class="sxs-lookup"><span data-stu-id="23809-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="23809-114">Quando uma chamada é feita, o cliente de avaliação do WaaS entra em contato com o serviço de avaliação do WaaS com os atributos do dispositivo e recebe um dossiê de informações aplicáveis ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23809-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="23809-115">Em seguida, o cliente usa essas informações em relação às informações coletadas sobre o dispositivo para realizar a avaliação.</span><span class="sxs-lookup"><span data-stu-id="23809-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="23809-116">Seu código deve ter privilégios de administrador para chamar a API de avaliação do WAAS.</span><span class="sxs-lookup"><span data-stu-id="23809-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="23809-117">Para obter mais detalhes sobre como desenvolver aplicativos que exigem privilégios de administrador, consulte [Este artigo](../secauthz/developing-applications-that-require-administrator-privilege.md).</span><span class="sxs-lookup"><span data-stu-id="23809-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
