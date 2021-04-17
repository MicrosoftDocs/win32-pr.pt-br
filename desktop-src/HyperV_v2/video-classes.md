---
description: Todas as máquinas virtuais refletem a presença de um controlador de vídeo S3 emulado e um controlador de vídeo mais rápido e sintético.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classes de vídeo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461303"
---
# <a name="video-classes"></a><span data-ttu-id="bc495-103">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="bc495-103">Video classes</span></span>

<span data-ttu-id="bc495-104">Todas as máquinas virtuais refletem a presença de um controlador de vídeo S3 emulado e um controlador de vídeo mais rápido e sintético.</span><span class="sxs-lookup"><span data-stu-id="bc495-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="bc495-105">Cada controlador de vídeo tem um objeto de cabeçalho de vídeo associado a ele.</span><span class="sxs-lookup"><span data-stu-id="bc495-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="bc495-106">Somente um controlador de vídeo pode estar ativo em uma máquina virtual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="bc495-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="bc495-107">Uma conexão de terminal está presente para cada sessão remota ativa conectada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc495-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="bc495-108">Veja a seguir as classes WMI de virtualização relacionadas ao vídeo.</span><span class="sxs-lookup"><span data-stu-id="bc495-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bc495-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bc495-109">In this section</span></span>



| <span data-ttu-id="bc495-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="bc495-110">Topic</span></span>                                                                                  | <span data-ttu-id="bc495-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc495-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc495-112">**Msvm \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="bc495-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="bc495-113">Representa o estado do controlador S3 emulado que está presente em cada configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc495-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="bc495-114">**Msvm \_ SyntheticDisplayController**</span><span class="sxs-lookup"><span data-stu-id="bc495-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="bc495-115">Representa o estado do controlador de vídeo sintético que está presente em cada configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc495-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="bc495-116">**Msvm \_ SystemTerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="bc495-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="bc495-117">Associa uma máquina virtual a uma conexão de terminal.</span><span class="sxs-lookup"><span data-stu-id="bc495-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="bc495-118">**Msvm \_ TerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="bc495-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="bc495-119">Indica o estado de uma sessão remota ativa que interage com uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc495-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="bc495-120">**Msvm \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="bc495-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="bc495-121">Descreve a superfície de desenho primária em um controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bc495-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="bc495-122">**Msvm \_ VideoHeadOnController**</span><span class="sxs-lookup"><span data-stu-id="bc495-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="bc495-123">Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.</span><span class="sxs-lookup"><span data-stu-id="bc495-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




