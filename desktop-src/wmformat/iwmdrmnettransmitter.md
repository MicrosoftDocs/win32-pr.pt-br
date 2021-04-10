---
title: Interface IWMDRMNetTransmitter
description: A interface IWMDRMNetTransmitter fornece métodos necessários para usar o DRM do Windows Media para dispositivos de rede como um transmissor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETTRANSMITTER IID como o parâmetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Formato de mídia do Windows da interface IWMDRMNetTransmitter
- Formato de mídia do Windows da interface IWMDRMNetTransmitter, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294266"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="beecb-106">Interface IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="beecb-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="beecb-107">A interface **IWMDRMNetTransmitter** fornece métodos necessários para usar o DRM do Windows Media para dispositivos de rede como um transmissor.</span><span class="sxs-lookup"><span data-stu-id="beecb-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="beecb-108">Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="beecb-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="beecb-109">Passe **\_ IWMDRMNetTransmitter IID** como o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="beecb-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="beecb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="beecb-110">Members</span></span>

<span data-ttu-id="beecb-111">A interface **IWMDRMNetTransmitter** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="beecb-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="beecb-112">**IWMDRMNetTransmitter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="beecb-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="beecb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="beecb-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="beecb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="beecb-114">Methods</span></span>

<span data-ttu-id="beecb-115">A interface **IWMDRMNetTransmitter** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="beecb-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="beecb-116">Método</span><span class="sxs-lookup"><span data-stu-id="beecb-116">Method</span></span>                                                                        | <span data-ttu-id="beecb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="beecb-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beecb-118">**GetLeafLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="beecb-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="beecb-119">Gera uma mensagem de resposta de licença de folha.</span><span class="sxs-lookup"><span data-stu-id="beecb-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="beecb-120">**GetRootLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="beecb-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="beecb-121">Gera uma mensagem de resposta de licença raiz</span><span class="sxs-lookup"><span data-stu-id="beecb-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="beecb-122">**SetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="beecb-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="beecb-123">Processa um desafio de licença enviado por um Microsoft Windows Media DRM para dispositivos de rede receptor</span><span class="sxs-lookup"><span data-stu-id="beecb-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="beecb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="beecb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beecb-125">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="beecb-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="beecb-126">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="beecb-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 

