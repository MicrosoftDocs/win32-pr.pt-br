---
title: Habilitando a sincronização com o Windows Media Player
description: Habilitando a sincronização com o Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Gerenciador de Dispositivos, sincronização com o Windows Media Player
- Gerenciador de Dispositivos, sincronização com o Windows Media Player
- Guia de programação, sincronização com o Windows Media Player
- provedores de serviços, sincronização com o Windows Media Player
- criando provedores de serviços, sincronização com o Windows Media Player
- sincronização com o Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770537"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="0b9fa-109">Habilitando a sincronização com o Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="0b9fa-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="0b9fa-110">Você pode habilitar um dispositivo para participar da sincronização automática com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0b9fa-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="0b9fa-111">A sincronização automática significa que, quando um dispositivo sincronizado designado pelo usuário se conectar ao computador, o Windows Media Player baixará, atualizará ou excluirá automaticamente arquivos do dispositivo sem a necessidade de nenhuma entrada adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b9fa-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="0b9fa-112">Por padrão, os seguintes dispositivos são sincronizados com o Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="0b9fa-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="0b9fa-113">Dispositivos MTP</span><span class="sxs-lookup"><span data-stu-id="0b9fa-113">MTP devices</span></span>
-   <span data-ttu-id="0b9fa-114">Dispositivos de armazenamento em massa</span><span class="sxs-lookup"><span data-stu-id="0b9fa-114">Mass-storage devices</span></span>
-   <span data-ttu-id="0b9fa-115">Dispositivos Windows CE (Windows Media Player 10 Mobile e posterior)</span><span class="sxs-lookup"><span data-stu-id="0b9fa-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="0b9fa-116">Para que qualquer outro dispositivo seja sincronizado com o Windows Media Player, os seguintes requisitos devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="0b9fa-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="0b9fa-117">O dispositivo deve anunciar uma interface de dispositivo PAP que é {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span><span class="sxs-lookup"><span data-stu-id="0b9fa-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="0b9fa-118">Os objetos de dispositivo retornados pelo provedor de serviços devem oferecer suporte à interface **IMDSPDevice3** .</span><span class="sxs-lookup"><span data-stu-id="0b9fa-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="0b9fa-119">O parâmetro de dispositivo UseExtendedWmdm deve ser definido como um valor **DWORD** de 1.</span><span class="sxs-lookup"><span data-stu-id="0b9fa-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="0b9fa-120">Consulte [parâmetros do dispositivo](device-parameters.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0b9fa-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="0b9fa-121">O provedor de serviços deve implementar as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="0b9fa-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="0b9fa-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="0b9fa-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="0b9fa-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="0b9fa-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="0b9fa-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="0b9fa-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="0b9fa-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b9fa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b9fa-126">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="0b9fa-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="0b9fa-127">**Parâmetros do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="0b9fa-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




