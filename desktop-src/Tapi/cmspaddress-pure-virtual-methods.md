---
description: Esses métodos devem ser substituídos por classes derivadas.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Métodos virtuais puros CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811014"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="b818c-103">Métodos virtuais puros CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="b818c-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="b818c-104">Esses métodos devem ser substituídos por classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="b818c-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="b818c-105">Métodos virtuais puros CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="b818c-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="b818c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b818c-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b818c-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="b818c-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="b818c-108">Método AddRef privado para o endereço.</span><span class="sxs-lookup"><span data-stu-id="b818c-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="b818c-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="b818c-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="b818c-110">Método de liberação particular para o endereço.</span><span class="sxs-lookup"><span data-stu-id="b818c-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="b818c-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="b818c-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="b818c-112">Chamado pela TAPI para criar um objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="b818c-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="b818c-113">A implementação na classe derivada deve simplesmente chamar a função [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="b818c-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="b818c-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="b818c-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="b818c-115">Chamado pela TAPI para desligar um objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="b818c-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="b818c-116">A implementação na classe derivada deve simplesmente chamar a função [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="b818c-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="b818c-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b818c-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="b818c-118">Obtém os tipos de mídia com suporte no MSP.</span><span class="sxs-lookup"><span data-stu-id="b818c-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="b818c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b818c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b818c-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="b818c-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



