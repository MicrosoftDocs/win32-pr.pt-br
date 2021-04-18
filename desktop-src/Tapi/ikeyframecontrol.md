---
description: A interface IKeyFrameControl é implementada pelo H. 323 MSP e está disponível somente em objetos de fluxo H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interface IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788065"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="406d2-103">Interface IKeyFrameControl</span><span class="sxs-lookup"><span data-stu-id="406d2-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="406d2-104">\[O **IKeyFrameControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="406d2-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="406d2-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="406d2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="406d2-106">A interface **IKeyFrameControl** é implementada pelo [H. 323 MSP](h323-msp.md) e está disponível somente em objetos de fluxo h. 323.</span><span class="sxs-lookup"><span data-stu-id="406d2-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="406d2-107">Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.</span><span class="sxs-lookup"><span data-stu-id="406d2-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="406d2-108">Ele tem dois métodos que permitem que o aplicativo peça ao ponto de extremidade remoto para atualizar a imagem de vídeo com um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="406d2-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="406d2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="406d2-109">Members</span></span>

<span data-ttu-id="406d2-110">A interface **IKeyFrameControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="406d2-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="406d2-111">**IKeyFrameControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="406d2-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="406d2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="406d2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="406d2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="406d2-113">Methods</span></span>

<span data-ttu-id="406d2-114">A interface **IKeyFrameControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="406d2-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="406d2-115">Método</span><span class="sxs-lookup"><span data-stu-id="406d2-115">Method</span></span>                                                                  | <span data-ttu-id="406d2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="406d2-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="406d2-117">**PeriodicUpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="406d2-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="406d2-118">Configura um temporizador no fluxo que solicitará atualizações de imagem periodicamente.</span><span class="sxs-lookup"><span data-stu-id="406d2-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="406d2-119">**UpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="406d2-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="406d2-120">Solicita que o remetente do vídeo atualize a imagem.</span><span class="sxs-lookup"><span data-stu-id="406d2-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="406d2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="406d2-121">Requirements</span></span>



| <span data-ttu-id="406d2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="406d2-122">Requirement</span></span> | <span data-ttu-id="406d2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="406d2-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="406d2-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="406d2-124">TAPI version</span></span><br/> | <span data-ttu-id="406d2-125">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="406d2-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="406d2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="406d2-126">Header</span></span><br/>       | <dl> <span data-ttu-id="406d2-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="406d2-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="406d2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="406d2-128">Library</span></span><br/>      | <dl> <span data-ttu-id="406d2-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="406d2-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="406d2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="406d2-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="406d2-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="406d2-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="406d2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="406d2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406d2-133">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="406d2-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

