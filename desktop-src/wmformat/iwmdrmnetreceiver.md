---
title: Interface IWMDRMNetReceiver
description: A interface IWMDRMNetReceiver fornece métodos necessários para usar o DRM do Microsoft Windows Media para dispositivos de rede como um receptor. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMNETRECEIVER IID como o parâmetro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Formato de mídia do Windows da interface IWMDRMNetReceiver
- Formato de mídia do Windows da interface IWMDRMNetReceiver, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365031"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="872f8-106">Interface IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="872f8-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="872f8-107">A interface **IWMDRMNetReceiver** fornece métodos necessários para usar o DRM do Microsoft Windows Media para dispositivos de rede como um receptor.</span><span class="sxs-lookup"><span data-stu-id="872f8-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="872f8-108">Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="872f8-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="872f8-109">Passe **\_ IWMDRMNetReceiver IID** como o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="872f8-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="872f8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="872f8-110">Members</span></span>

<span data-ttu-id="872f8-111">A interface **IWMDRMNetReceiver** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="872f8-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="872f8-112">**IWMDRMNetReceiver** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="872f8-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="872f8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="872f8-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="872f8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="872f8-114">Methods</span></span>

<span data-ttu-id="872f8-115">A interface **IWMDRMNetReceiver** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="872f8-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="872f8-116">Método</span><span class="sxs-lookup"><span data-stu-id="872f8-116">Method</span></span>                                                                               | <span data-ttu-id="872f8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="872f8-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="872f8-118">**GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="872f8-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="872f8-119">Gera um desafio de licença que é enviado ao transmissor ao solicitar conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="872f8-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="872f8-120">**GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="872f8-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="872f8-121">Gera um desafio de registro que é enviado para o transmissor quando o receptor está se registrando ou revalidando.</span><span class="sxs-lookup"><span data-stu-id="872f8-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="872f8-122">**ProcessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="872f8-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="872f8-123">Processa a resposta de licença enviada pelo transmissor em resposta a um desafio de licença.</span><span class="sxs-lookup"><span data-stu-id="872f8-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="872f8-124">**ProcessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="872f8-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="872f8-125">Processa a resposta de registro enviada pelo transmissor em resposta a um desafio de registro.</span><span class="sxs-lookup"><span data-stu-id="872f8-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="872f8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="872f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872f8-127">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="872f8-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="872f8-128">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="872f8-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="872f8-129">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="872f8-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





