---
description: A interface ITParticipantControl é implementada pelo IPConf MSP.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interface ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780123"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="39097-103">Interface ITParticipantControl</span><span class="sxs-lookup"><span data-stu-id="39097-103">ITParticipantControl interface</span></span>

<span data-ttu-id="39097-104">\[O **ITParticipantControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="39097-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="39097-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="39097-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="39097-106">A interface **ITParticipantControl** é implementada pelo IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="39097-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="39097-107">Essa interface é exposta no objeto de chamada.</span><span class="sxs-lookup"><span data-stu-id="39097-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="39097-108">Essa interface permite que um aplicativo recupere ponteiros para os participantes em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="39097-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="39097-109">A interface **ITParticipantControl** é criada chamando **QueryInterface** no [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="39097-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="39097-110">Membros</span><span class="sxs-lookup"><span data-stu-id="39097-110">Members</span></span>

<span data-ttu-id="39097-111">A interface **ITParticipantControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="39097-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="39097-112">**ITParticipantControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39097-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="39097-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="39097-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="39097-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="39097-114">Methods</span></span>

<span data-ttu-id="39097-115">A interface **ITParticipantControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="39097-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="39097-116">Método</span><span class="sxs-lookup"><span data-stu-id="39097-116">Method</span></span>                                                                      | <span data-ttu-id="39097-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="39097-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39097-118">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="39097-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="39097-119">Enumera os participantes atualmente envolvidos na conferência.</span><span class="sxs-lookup"><span data-stu-id="39097-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="39097-120">**obter \_ participantes**</span><span class="sxs-lookup"><span data-stu-id="39097-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="39097-121">Cria uma coleção de participantes associados à conferência atual.</span><span class="sxs-lookup"><span data-stu-id="39097-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="39097-122">Fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="39097-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39097-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39097-123">Requirements</span></span>



| <span data-ttu-id="39097-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39097-124">Requirement</span></span> | <span data-ttu-id="39097-125">Valor</span><span class="sxs-lookup"><span data-stu-id="39097-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39097-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="39097-126">TAPI version</span></span><br/> | <span data-ttu-id="39097-127">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="39097-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="39097-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39097-128">Header</span></span><br/>       | <dl> <span data-ttu-id="39097-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="39097-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="39097-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39097-130">Library</span></span><br/>      | <dl> <span data-ttu-id="39097-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39097-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="39097-132">DLL</span><span class="sxs-lookup"><span data-stu-id="39097-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="39097-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39097-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

