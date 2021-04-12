---
title: Objeto do agente de revogação de licença
description: Objeto do agente de revogação de licença
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- SDK do Windows Media Format, objetos do agente de revogação de licença
- ASF (Advanced Systems Format), objetos de agente de revogação de licença
- ASF (formato de sistemas avançados), objetos de agente de revogação de licença
- objetos, objetos do agente de revogação de licença
- revogação de licença, objetos do agente de revogação de licença
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365537"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="50d03-108">Objeto do agente de revogação de licença</span><span class="sxs-lookup"><span data-stu-id="50d03-108">License Revocation Agent Object</span></span>

<span data-ttu-id="50d03-109">O objeto do agente de revogação de licença gerencia o lado do cliente da revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="50d03-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="50d03-110">A revogação de licenças é o processo pelo qual um servidor de licença pode remover licenças do repositório de licenças no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="50d03-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="50d03-111">O processo envolve a passagem de várias mensagens entre o aplicativo cliente e o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="50d03-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="50d03-112">Os métodos expostos neste objeto processam e geram essas mensagens.</span><span class="sxs-lookup"><span data-stu-id="50d03-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="50d03-113">O objeto do agente de revogação de licença é criado pela função [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , que define um ponteiro para uma interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .</span><span class="sxs-lookup"><span data-stu-id="50d03-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="50d03-114">**IUnknown** e **IWMLicenseRevocationAgent** são as únicas interfaces suportadas por este objeto.</span><span class="sxs-lookup"><span data-stu-id="50d03-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50d03-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50d03-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50d03-116">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="50d03-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




