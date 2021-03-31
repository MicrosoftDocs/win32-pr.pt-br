---
title: Conjunto de comandos MIDI Sequencer
description: Conjunto de comandos MIDI Sequencer
ms.assetid: 8f5af706-0674-4ed1-855f-22f8d74361fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bac1f9ca26a8e7e7e636c19ffa92d05281e16bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916213"
---
# <a name="midi-sequencer-command-set"></a><span data-ttu-id="e1572-103">Conjunto de comandos MIDI Sequencer</span><span class="sxs-lookup"><span data-stu-id="e1572-103">MIDI Sequencer Command Set</span></span>

<span data-ttu-id="e1572-104">O Sequencer MIDI dá suporte ao seguinte conjunto de comandos.</span><span class="sxs-lookup"><span data-stu-id="e1572-104">The MIDI sequencer supports the following set of commands.</span></span>



| <span data-ttu-id="e1572-105">Formulário de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e1572-105">String form</span></span>                      | <span data-ttu-id="e1572-106">Formulário de mensagem</span><span class="sxs-lookup"><span data-stu-id="e1572-106">Message form</span></span>                              |
|----------------------------------|-------------------------------------------|
| [<span data-ttu-id="e1572-107">**interrupção**</span><span class="sxs-lookup"><span data-stu-id="e1572-107">**break**</span></span>](break.md)           | [<span data-ttu-id="e1572-108">**interrupção de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-108">**MCI\_BREAK**</span></span>](mci-break.md)           |
| [<span data-ttu-id="e1572-109">**recursos**</span><span class="sxs-lookup"><span data-stu-id="e1572-109">**capability**</span></span>](capability.md) | [<span data-ttu-id="e1572-110">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="e1572-110">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md) |
| [<span data-ttu-id="e1572-111">**inclui**</span><span class="sxs-lookup"><span data-stu-id="e1572-111">**close**</span></span>](close.md)           | [<span data-ttu-id="e1572-112">**fechamento de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-112">**MCI\_CLOSE**</span></span>](mci-close.md)           |
| [<span data-ttu-id="e1572-113">**detalhes**</span><span class="sxs-lookup"><span data-stu-id="e1572-113">**info**</span></span>](info.md)             | [<span data-ttu-id="e1572-114">**informações do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-114">**MCI\_INFO**</span></span>](mci-info.md)             |
| [<span data-ttu-id="e1572-115">**abrir**</span><span class="sxs-lookup"><span data-stu-id="e1572-115">**open**</span></span>](open.md)             | [<span data-ttu-id="e1572-116">**MCI \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="e1572-116">**MCI\_OPEN**</span></span>](mci-open.md)             |
| [<span data-ttu-id="e1572-117">**temporariamente**</span><span class="sxs-lookup"><span data-stu-id="e1572-117">**pause**</span></span>](pause.md)           | [<span data-ttu-id="e1572-118">**pausa de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-118">**MCI\_PAUSE**</span></span>](mci-pause.md)           |
| [<span data-ttu-id="e1572-119">**reproduzir**</span><span class="sxs-lookup"><span data-stu-id="e1572-119">**play**</span></span>](play.md)             | [<span data-ttu-id="e1572-120">**\_reprodução MCI**</span><span class="sxs-lookup"><span data-stu-id="e1572-120">**MCI\_PLAY**</span></span>](mci-play.md)             |
| [<span data-ttu-id="e1572-121">**gravável**</span><span class="sxs-lookup"><span data-stu-id="e1572-121">**record**</span></span>](record.md)         | [<span data-ttu-id="e1572-122">**\_registro MCI**</span><span class="sxs-lookup"><span data-stu-id="e1572-122">**MCI\_RECORD**</span></span>](mci-record.md)         |
| [<span data-ttu-id="e1572-123">**Volte**</span><span class="sxs-lookup"><span data-stu-id="e1572-123">**resume**</span></span>](resume.md)         | [<span data-ttu-id="e1572-124">**retomar MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-124">**MCI\_RESUME**</span></span>](mci-resume.md)         |
| [<span data-ttu-id="e1572-125">**Guarde**</span><span class="sxs-lookup"><span data-stu-id="e1572-125">**save**</span></span>](save.md)             | [<span data-ttu-id="e1572-126">**\_salvar MCI**</span><span class="sxs-lookup"><span data-stu-id="e1572-126">**MCI\_SAVE**</span></span>](mci-save.md)             |
| [<span data-ttu-id="e1572-127">**Procure**</span><span class="sxs-lookup"><span data-stu-id="e1572-127">**seek**</span></span>](seek.md)             | [<span data-ttu-id="e1572-128">**busca de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-128">**MCI\_SEEK**</span></span>](mci-seek.md)             |
| [<span data-ttu-id="e1572-129">**Definição**</span><span class="sxs-lookup"><span data-stu-id="e1572-129">**set**</span></span>](set.md)               | [<span data-ttu-id="e1572-130">**conjunto de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-130">**MCI\_SET**</span></span>](mci-set.md)               |
| [<span data-ttu-id="e1572-131">**status**</span><span class="sxs-lookup"><span data-stu-id="e1572-131">**status**</span></span>](status.md)         | [<span data-ttu-id="e1572-132">**STATUS do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-132">**MCI\_STATUS**</span></span>](mci-status.md)         |
| [<span data-ttu-id="e1572-133">**deixar**</span><span class="sxs-lookup"><span data-stu-id="e1572-133">**stop**</span></span>](stop.md)             | [<span data-ttu-id="e1572-134">**parada do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-134">**MCI\_STOP**</span></span>](mci-stop.md)             |
| [<span data-ttu-id="e1572-135">SysInfo</span><span class="sxs-lookup"><span data-stu-id="e1572-135">sysinfo</span></span>](sysinfo.md)           | [<span data-ttu-id="e1572-136">**SysInfo do MCI \_**</span><span class="sxs-lookup"><span data-stu-id="e1572-136">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)       |



 

 

 




