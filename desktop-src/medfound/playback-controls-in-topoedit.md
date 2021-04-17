---
description: Controles de reprodução no TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reprodução no TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550441"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="50500-103">Controles de reprodução no TopoEdit</span><span class="sxs-lookup"><span data-stu-id="50500-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="50500-104">Depois que uma topologia é resolvida, ela é enfileirada na sessão de mídia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="50500-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="50500-105">O TopoEdit fornece controle de transporte para alterar o estado da topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="50500-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="50500-106">A tabela a seguir mostra o comando de menu/barra de ferramentas e o método equivalente Media Foundation para cada operação.</span><span class="sxs-lookup"><span data-stu-id="50500-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="50500-107">Comando de menu/barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="50500-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="50500-108">Método de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50500-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="50500-109">No menu **controles** , clique em **reproduzir**. \[ nova linha \] ou \[ nova linha \] clique no botão **reproduzir** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão de reprodução](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="50500-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="50500-110">**IMFMediaSession:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="50500-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="50500-111">No menu **controles** , clique em **parar**. \[ nova linha \] ou \[ nova linha \] clique no botão **parar** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão parar](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="50500-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="50500-112">**IMFMediaSession:: Stop**</span><span class="sxs-lookup"><span data-stu-id="50500-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="50500-113">No menu **controles** , clique em **Pausar**. \[ nova linha \] , ou \[ nova linha, \] clique no botão **Pausar** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão Pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="50500-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="50500-114">**IMFMediaSession::P ause**</span><span class="sxs-lookup"><span data-stu-id="50500-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="50500-115">Para obter informações sobre como controlar a reprodução programaticamente usando APIs Media Foundation, consulte [como controlar os Estados de apresentação](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="50500-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="50500-116">Atingir</span><span class="sxs-lookup"><span data-stu-id="50500-116">Seeking</span></span>

<span data-ttu-id="50500-117">Se a topologia for pesquisável, você poderá buscar usando a barra de busca (mostrada na imagem a seguir) para especificar um local na linha do tempo da topologia para começar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="50500-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![captura de tela da barra de busca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="50500-119">Se a origem da mídia for pesquisável, o comando Stop também buscará a topologia de volta ao início do fluxo.</span><span class="sxs-lookup"><span data-stu-id="50500-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="50500-120">Alterando a taxa de reprodução</span><span class="sxs-lookup"><span data-stu-id="50500-120">Changing the Playback Rate</span></span>

<span data-ttu-id="50500-121">Se a fonte de mídia subjacente para a topologia oferecer suporte a várias taxas de reprodução, você poderá usar a barra de taxa para alterar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="50500-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="50500-122">Para avançar rapidamente uma topologia na sessão de mídia, aumente a taxa arrastando o controle deslizante para a direita, conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="50500-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![captura de tela da barra de taxas](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="50500-124">Nesta versão, o TopoEdit dá suporte apenas a tarifas positivas.</span><span class="sxs-lookup"><span data-stu-id="50500-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="50500-125">Não há suporte para reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="50500-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="50500-126">Para obter informações sobre como alterar a taxa de reprodução programaticamente usando APIs Media Foundation, consulte [sobre o controle de taxa](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="50500-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50500-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50500-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50500-128">TopoEdit menus</span><span class="sxs-lookup"><span data-stu-id="50500-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="50500-129">Barra de ferramentas TopoEdit</span><span class="sxs-lookup"><span data-stu-id="50500-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="50500-130">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="50500-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



