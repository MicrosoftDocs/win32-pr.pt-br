---
description: Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091043"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="133c0-103">OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS</span><span class="sxs-lookup"><span data-stu-id="133c0-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="133c0-104">Define o nível de proteção de HDCP para reprodução de DVD, seguindo as regras de sistema de embaralhamento de conteúdo de DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="133c0-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="133c0-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="133c0-105">Requirement</span></span> | <span data-ttu-id="133c0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="133c0-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="133c0-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="133c0-107">Command GUID</span></span> | <span data-ttu-id="133c0-108">OPM \_ define \_ o \_ nível \_ \_ de proteção de acordo \_ \_ com o DVD do CSS</span><span class="sxs-lookup"><span data-stu-id="133c0-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="133c0-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="133c0-109">Input data</span></span>   | <span data-ttu-id="133c0-110">Uma estrutura de [**parâmetros de nível de proteção dos OPMS \_ definidos \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="133c0-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="133c0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="133c0-111">Remarks</span></span>

<span data-ttu-id="133c0-112">Esse comando é usado para definir High-Bandwidth Proteção de Conteúdo Digital (HDCP) ao reproduzir DVDs padrão.</span><span class="sxs-lookup"><span data-stu-id="133c0-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="133c0-113">Ao contrário do comando de [**\_ nível de \_ proteção \_ do OPM definido**](opm-set-protection-level.md) , se HDCP não puder ser definido por algum motivo, esse comando não interromperá a reprodução.</span><span class="sxs-lookup"><span data-stu-id="133c0-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="133c0-114">(As regras de DVD CSS contêm um provisionamento de "melhor esforço" para os jogadores.) Caso contrário, esse comando é idêntico ao comando de **nível de proteção de OPM \_ set \_ Protection \_** .</span><span class="sxs-lookup"><span data-stu-id="133c0-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="133c0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="133c0-115">Requirements</span></span>



| <span data-ttu-id="133c0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="133c0-116">Requirement</span></span> | <span data-ttu-id="133c0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="133c0-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="133c0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="133c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="133c0-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="133c0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="133c0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="133c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="133c0-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="133c0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="133c0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="133c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="133c0-123"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="133c0-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="133c0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="133c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133c0-125">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="133c0-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="133c0-126">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="133c0-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




