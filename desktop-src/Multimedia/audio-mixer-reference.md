---
title: Referência do mixer de áudio
description: Referência do mixer de áudio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- áudio de multimídia, mixers de áudio
- áudio, mixers de áudio
- áudio de multimídia, referência de mixer
- áudio, referência de mixer
- mixers de áudio, referência
- mixers, referência
- referência para mixers de áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162240"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="10ac2-110">Referência do mixer de áudio</span><span class="sxs-lookup"><span data-stu-id="10ac2-110">Audio Mixer Reference</span></span>

<span data-ttu-id="10ac2-111">Esta seção descreve as funções, as estruturas e as mensagens associadas aos mixers de áudio.</span><span class="sxs-lookup"><span data-stu-id="10ac2-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="10ac2-112">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="10ac2-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="10ac2-113">Consultando dispositivos</span><span class="sxs-lookup"><span data-stu-id="10ac2-113">Querying Devices</span></span>

-   [<span data-ttu-id="10ac2-114">**MIXERCAPS**</span><span class="sxs-lookup"><span data-stu-id="10ac2-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="10ac2-115">**mixerGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="10ac2-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="10ac2-116">**mixerGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="10ac2-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="10ac2-117">Abrindo e fechando</span><span class="sxs-lookup"><span data-stu-id="10ac2-117">Opening and Closing</span></span>

-   [<span data-ttu-id="10ac2-118">**mixerClose**</span><span class="sxs-lookup"><span data-stu-id="10ac2-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="10ac2-119">**mixerOpen**</span><span class="sxs-lookup"><span data-stu-id="10ac2-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="10ac2-120">Recuperando identificadores do mixer</span><span class="sxs-lookup"><span data-stu-id="10ac2-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="10ac2-121">**mixerGetID**</span><span class="sxs-lookup"><span data-stu-id="10ac2-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="10ac2-122">Recuperando controles de linha</span><span class="sxs-lookup"><span data-stu-id="10ac2-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="10ac2-123">**MIXERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="10ac2-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="10ac2-124">**mixerGetLineControls**</span><span class="sxs-lookup"><span data-stu-id="10ac2-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="10ac2-125">**MIXERLINECONTROLS**</span><span class="sxs-lookup"><span data-stu-id="10ac2-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="10ac2-126">Alterando atributos de controle</span><span class="sxs-lookup"><span data-stu-id="10ac2-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="10ac2-127">**MIXERCONTROLDETAILS**</span><span class="sxs-lookup"><span data-stu-id="10ac2-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="10ac2-128">[**MIXERCONTROLDETAILS \_ booliano**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10ac2-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="10ac2-129">[**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10ac2-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="10ac2-130">[**MIXERCONTROLDETAILS \_ assinado**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10ac2-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="10ac2-131">[**MIXERCONTROLDETAILS \_ não assinado**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10ac2-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="10ac2-132">**mixerGetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="10ac2-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="10ac2-133">**mixerSetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="10ac2-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="10ac2-134">Recuperando informações de linha</span><span class="sxs-lookup"><span data-stu-id="10ac2-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="10ac2-135">**mixerGetLineInfo**</span><span class="sxs-lookup"><span data-stu-id="10ac2-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="10ac2-136">**MIXER**</span><span class="sxs-lookup"><span data-stu-id="10ac2-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="10ac2-137">**\_alteração de \_ controle de MIXM mm \_**</span><span class="sxs-lookup"><span data-stu-id="10ac2-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="10ac2-138">**\_alteração de \_ linha \_ MIXM mm**</span><span class="sxs-lookup"><span data-stu-id="10ac2-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="10ac2-139">Enviando mensagens de User-Defined</span><span class="sxs-lookup"><span data-stu-id="10ac2-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="10ac2-140">**mixerMessage**</span><span class="sxs-lookup"><span data-stu-id="10ac2-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="10ac2-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10ac2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10ac2-142">Referência do mixer de áudio</span><span class="sxs-lookup"><span data-stu-id="10ac2-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 