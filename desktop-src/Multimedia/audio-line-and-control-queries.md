---
title: Consultas de linha e controle de áudio
description: Consultas de linha e controle de áudio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- áudio de multimídia, controles de mixer
- áudio, controles de mixer
- mixers de áudio, linhas de áudio
- linhas de áudio
- mixers de áudio, controles
- mixers, controles
- mixers, linhas de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640546"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="7806d-110">Consultas de linha e controle de áudio</span><span class="sxs-lookup"><span data-stu-id="7806d-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="7806d-111">Os serviços de mixer fornecem funções para determinar informações sobre linhas de áudio, controles de linha de áudio e detalhes de controle.</span><span class="sxs-lookup"><span data-stu-id="7806d-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="7806d-112">Os serviços também fornecem funções para definir detalhes de controle.</span><span class="sxs-lookup"><span data-stu-id="7806d-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="7806d-113">Você pode usar a função [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) para recuperar informações sobre uma linha de áudio especificada.</span><span class="sxs-lookup"><span data-stu-id="7806d-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="7806d-114">Essa função preenche a estrutura de [**mixer**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) para uma linha de áudio de origem especificada, uma linha de áudio de destino ou um identificador de linha.</span><span class="sxs-lookup"><span data-stu-id="7806d-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="7806d-115">A estrutura inclui o número de linha de destino, o número de canais na linha de áudio, bem como um nome curto e longo para a linha de áudio.</span><span class="sxs-lookup"><span data-stu-id="7806d-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="7806d-116">A função [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera informações gerais sobre um ou mais controles associados a uma linha de áudio.</span><span class="sxs-lookup"><span data-stu-id="7806d-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="7806d-117">Essa função preenche a estrutura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) com informações sobre o controle ou controles especificados.</span><span class="sxs-lookup"><span data-stu-id="7806d-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="7806d-118">Você pode usar **mixerGetLineControls** para recuperar as propriedades de controle de um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7806d-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="7806d-119">Todos os controles para uma linha de origem especificada</span><span class="sxs-lookup"><span data-stu-id="7806d-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="7806d-120">Um controle especificado para uma linha de origem especificada</span><span class="sxs-lookup"><span data-stu-id="7806d-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="7806d-121">O primeiro controle de uma classe específica para uma linha de origem especificada</span><span class="sxs-lookup"><span data-stu-id="7806d-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="7806d-122">A função [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera as propriedades de um único controle associado a uma linha de áudio.</span><span class="sxs-lookup"><span data-stu-id="7806d-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="7806d-123">Essa função preenche a estrutura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) com os valores atuais de um controle.</span><span class="sxs-lookup"><span data-stu-id="7806d-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="7806d-124">A função [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa o conteúdo da estrutura **MIXERCONTROLDETAILS** para definir as propriedades do controle especificado.</span><span class="sxs-lookup"><span data-stu-id="7806d-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="7806d-125">Você deve garantir que todos os membros desta estrutura sejam preenchidos antes de chamar **mixerSetControlDetails**.</span><span class="sxs-lookup"><span data-stu-id="7806d-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 