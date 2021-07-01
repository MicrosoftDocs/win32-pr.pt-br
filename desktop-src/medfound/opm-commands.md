---
description: Comandos OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119141"
---
# <a name="opm-commands"></a><span data-ttu-id="d6383-103">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="d6383-103">OPM Commands</span></span>

<span data-ttu-id="d6383-104">Esta seção lista os comandos disponíveis para o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="d6383-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="d6383-105">Para enviar um comando OPM, chame [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="d6383-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="d6383-106">Para cada comando, as informações a seguir são listadas.</span><span class="sxs-lookup"><span data-stu-id="d6383-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="d6383-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d6383-107">Value</span></span>             | <span data-ttu-id="d6383-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6383-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6383-109">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="d6383-109">Command GUID</span></span> | <span data-ttu-id="d6383-110">Identifica o comando.</span><span class="sxs-lookup"><span data-stu-id="d6383-110">Identifies the command.</span></span> <span data-ttu-id="d6383-111">Defina o membro **guidSetting** da estrutura de [**configuração de \_ \_ parâmetros de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6383-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="d6383-112">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="d6383-112">Input data</span></span>   | <span data-ttu-id="d6383-113">Especifica como interpretar a matriz **abParameters** na estrutura de [**\_ \_ parâmetros de configuração de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="d6383-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="d6383-114">Os comandos a seguir são definidos:</span><span class="sxs-lookup"><span data-stu-id="d6383-114">The following commands are defined:</span></span>



| <span data-ttu-id="d6383-115">Comando</span><span class="sxs-lookup"><span data-stu-id="d6383-115">Command</span></span>                                                                                                       | <span data-ttu-id="d6383-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6383-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6383-117">**OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="d6383-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="d6383-118">Especifica informações sobre o sinal de vídeo, além do nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="d6383-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="d6383-119">**OPM \_ definido \_ SRM de HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="d6383-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="d6383-120">Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).</span><span class="sxs-lookup"><span data-stu-id="d6383-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="d6383-121">**OPM \_ definir \_ nível de proteção \_**</span><span class="sxs-lookup"><span data-stu-id="d6383-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="d6383-122">Define o nível de proteção para um mecanismo de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="d6383-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="d6383-123">**OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS**</span><span class="sxs-lookup"><span data-stu-id="d6383-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="d6383-124">Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="d6383-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d6383-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6383-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6383-126">Referência de programação de OPM</span><span class="sxs-lookup"><span data-stu-id="d6383-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d6383-127">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="d6383-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



