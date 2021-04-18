---
description: Comandos OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814164"
---
# <a name="opm-commands"></a><span data-ttu-id="32d53-103">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="32d53-103">OPM Commands</span></span>

<span data-ttu-id="32d53-104">Esta seção lista os comandos disponíveis para o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="32d53-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="32d53-105">Para enviar um comando OPM, chame [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="32d53-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="32d53-106">Para cada comando, as informações a seguir são listadas.</span><span class="sxs-lookup"><span data-stu-id="32d53-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d53-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="32d53-107">Command GUID</span></span> | <span data-ttu-id="32d53-108">Identifica o comando.</span><span class="sxs-lookup"><span data-stu-id="32d53-108">Identifies the command.</span></span> <span data-ttu-id="32d53-109">Defina o membro **guidSetting** da estrutura de [**configuração de \_ \_ parâmetros de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a esse valor.</span><span class="sxs-lookup"><span data-stu-id="32d53-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="32d53-110">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="32d53-110">Input data</span></span>   | <span data-ttu-id="32d53-111">Especifica como interpretar a matriz **abParameters** na estrutura de [**\_ \_ parâmetros de configuração de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="32d53-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="32d53-112">Os comandos a seguir são definidos:</span><span class="sxs-lookup"><span data-stu-id="32d53-112">The following commands are defined:</span></span>



| <span data-ttu-id="32d53-113">Comando</span><span class="sxs-lookup"><span data-stu-id="32d53-113">Command</span></span>                                                                                                       | <span data-ttu-id="32d53-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="32d53-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32d53-115">**OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="32d53-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="32d53-116">Especifica informações sobre o sinal de vídeo, além do nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="32d53-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="32d53-117">**OPM \_ definido \_ SRM de HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="32d53-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="32d53-118">Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).</span><span class="sxs-lookup"><span data-stu-id="32d53-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="32d53-119">**OPM \_ definir \_ nível de proteção \_**</span><span class="sxs-lookup"><span data-stu-id="32d53-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="32d53-120">Define o nível de proteção para um mecanismo de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="32d53-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="32d53-121">**OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS**</span><span class="sxs-lookup"><span data-stu-id="32d53-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="32d53-122">Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="32d53-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="32d53-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32d53-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d53-124">Referência de programação de OPM</span><span class="sxs-lookup"><span data-stu-id="32d53-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="32d53-125">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="32d53-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



