---
title: Sobre a cópia de CD
description: Sobre a cópia de CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, sobre
- copiando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105760904"
---
# <a name="about-cd-ripping"></a><span data-ttu-id="3cb27-112">Sobre a cópia de CD</span><span class="sxs-lookup"><span data-stu-id="3cb27-112">About CD Ripping</span></span>

<span data-ttu-id="3cb27-113">O SDK do Windows Media Player 11 introduz uma nova funcionalidade para copiar faixas de áudio de CDs para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="3cb27-113">The Windows Media Player 11 SDK introduces new functionality for copying audio tracks from CDs to the user's computer.</span></span> <span data-ttu-id="3cb27-114">Esse processo é chamado de *cópia de CDs*.</span><span class="sxs-lookup"><span data-stu-id="3cb27-114">This process is called *ripping*.</span></span>

<span data-ttu-id="3cb27-115">Quando você copia faixas de áudio usando as interfaces do SDK do Windows Media Player, as faixas de música resultantes são criadas usando as configurações definidas pelo usuário na caixa de diálogo **Opções** do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3cb27-115">When you rip audio tracks by using the Windows Media Player SDK interfaces, the resulting music tracks are created by using the settings that the user defined in the Windows Media Player **Options** dialog box.</span></span>

<span data-ttu-id="3cb27-116">Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="3cb27-116">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="3cb27-117">Você recupera um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="3cb27-117">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span> <span data-ttu-id="3cb27-118">Usando os métodos **Count** e **Item** , você pode iterar a coleção para recuperar um ponteiro de interface **IWMPCDROM** para cada unidade de CD no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="3cb27-118">By using the **count** and **item** methods, you can iterate the collection to retrieve an **IWMPCdrom** interface pointer for each CD drive on the user's computer.</span></span> <span data-ttu-id="3cb27-119">A interface **IWMPCdrom** representa uma unidade de CD individual.</span><span class="sxs-lookup"><span data-stu-id="3cb27-119">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="3cb27-120">Antes de começar a copiar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface **IWMPCdromRip** .</span><span class="sxs-lookup"><span data-stu-id="3cb27-120">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the **IWMPCdromRip** interface.</span></span>

<span data-ttu-id="3cb27-121">Para iniciar a operação de cópia de CDs, basta chamar [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="3cb27-121">To start the ripping operation, simply call [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span> <span data-ttu-id="3cb27-122">Você pode monitorar o progresso da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="3cb27-122">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="3cb27-123">Esse método recupera um valor de progresso para toda a operação de cópia de CDs.</span><span class="sxs-lookup"><span data-stu-id="3cb27-123">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="3cb27-124">O valor recuperado é um número que representa a porcentagem de cópia concluída.</span><span class="sxs-lookup"><span data-stu-id="3cb27-124">The value retrieved is a number that represents the percentage of ripping completed.</span></span> <span data-ttu-id="3cb27-125">Você pode monitorar o estado da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="3cb27-125">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="3cb27-126">Esse método recupera um valor de enumeração [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="3cb27-126">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="3cb27-127">Você também pode monitorar o estado da operação de cópia de CDs manipulando o evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="3cb27-127">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="3cb27-128">Você deve ter cuidado para comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de cópia para garantir que o evento foi gerado pela operação.</span><span class="sxs-lookup"><span data-stu-id="3cb27-128">You should be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation to ensure that the event was raised by your operation.</span></span> <span data-ttu-id="3cb27-129">Você pode interromper a operação de cópia de CDs chamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="3cb27-129">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>

<span data-ttu-id="3cb27-130">Para receber notificações de erro sobre uma operação de cópia de CDs, você pode manipular o evento [IWMPEvents3:: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) .</span><span class="sxs-lookup"><span data-stu-id="3cb27-130">To receive error notifications about a ripping operation, you can handle the [IWMPEvents3::CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) event.</span></span> <span data-ttu-id="3cb27-131">Assim como **CdromRipStateChange**, esse evento fornece um ponteiro de interface **IWMPCdromRip** que representa a operação de cópia de CDs que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="3cb27-131">Like **CdromRipStateChange**, this event provides an **IWMPCdromRip** interface pointer that represents the ripping operation that raised the event.</span></span> <span data-ttu-id="3cb27-132">O evento também fornece um ponteiro **IDispatch** que representa o item de mídia que disparou o evento.</span><span class="sxs-lookup"><span data-stu-id="3cb27-132">The event also provides an **IDispatch** pointer that represents the media item that raised the event.</span></span> <span data-ttu-id="3cb27-133">Você pode chamar **QueryInterface** por meio desse ponteiro para recuperar um ponteiro **IWMPMedia** .</span><span class="sxs-lookup"><span data-stu-id="3cb27-133">You can call **QueryInterface** through this pointer to retrieve an **IWMPMedia** pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cb27-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cb27-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb27-135">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="3cb27-135">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




