---
title: Serviços de Área de Trabalho Remota interfaces AudioEndpoint
description: As interfaces a seguir são usadas com a API AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761324"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="39f80-103">Serviços de Área de Trabalho Remota interfaces AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f80-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="39f80-104">As interfaces a seguir são usadas com a API AudioEndpoint.</span><span class="sxs-lookup"><span data-stu-id="39f80-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="39f80-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="39f80-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="39f80-106">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="39f80-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="39f80-107">Inicializa um objeto de ponto de extremidade do dispositivo e obtém os recursos do dispositivo que ele representa.</span><span class="sxs-lookup"><span data-stu-id="39f80-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="39f80-108">**IAudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="39f80-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="39f80-109">Fornece informações para o mecanismo de áudio sobre um ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="39f80-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="39f80-110">Essa interface é implementada por um ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="39f80-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="39f80-111">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="39f80-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="39f80-112">Controla o estado de fluxo de um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="39f80-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="39f80-113">**IAudioEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="39f80-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="39f80-114">Obtém a diferença entre as posições de leitura e gravação atuais no buffer de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="39f80-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="39f80-115">**IAudioInputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="39f80-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="39f80-116">Obtém o buffer de entrada para cada passagem de processamento.</span><span class="sxs-lookup"><span data-stu-id="39f80-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="39f80-117">**IAudioOutputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="39f80-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="39f80-118">Obtém o buffer de saída para cada passagem de processamento.</span><span class="sxs-lookup"><span data-stu-id="39f80-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39f80-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="39f80-119">Remarks</span></span>

<span data-ttu-id="39f80-120">O Serviços de Área de Trabalho Remota API AudioEndpoint é para uso em cenários de Área de Trabalho Remota; Não é para aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="39f80-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




