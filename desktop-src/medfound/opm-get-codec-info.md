---
description: Obtém o valor de mérito de um codec de hardware.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164905"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="60046-103">\_informações do \_ codec de obtenção de OPM \_</span><span class="sxs-lookup"><span data-stu-id="60046-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="60046-104">Obtém o valor de mérito de um codec de hardware.</span><span class="sxs-lookup"><span data-stu-id="60046-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="60046-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="60046-105">Requirement</span></span> | <span data-ttu-id="60046-106">Valor</span><span class="sxs-lookup"><span data-stu-id="60046-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60046-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="60046-107">Request GUID</span></span> | <span data-ttu-id="60046-108">**\_informações do \_ codec de obtenção de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="60046-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="60046-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="60046-109">Input data</span></span>   | <span data-ttu-id="60046-110">Uma estrutura de [**parâmetros de informações de codec de \_ obtenção \_ \_ \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="60046-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="60046-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="60046-111">Return data</span></span>  | <span data-ttu-id="60046-112">Uma estrutura de informação de informações do [**\_ codec de \_ \_ informações \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)</span><span class="sxs-lookup"><span data-stu-id="60046-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="60046-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="60046-113">Remarks</span></span>

<span data-ttu-id="60046-114">Embora esse comando use a interface do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM), ele se aplica somente a codificadores de hardware e decodificadores.</span><span class="sxs-lookup"><span data-stu-id="60046-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="60046-115">Ele não se aplica a dispositivos de saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="60046-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="60046-116">Em geral, você não deve usar esse comando diretamente.</span><span class="sxs-lookup"><span data-stu-id="60046-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="60046-117">Para obter o valor de mérito para um codec de hardware, chame a função [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="60046-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="60046-118">Essa função executa todas as chamadas de OPM necessárias para enviar o comando **OPM \_ Get \_ codec \_ info** .</span><span class="sxs-lookup"><span data-stu-id="60046-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="60046-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60046-119">Requirements</span></span>



| <span data-ttu-id="60046-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="60046-120">Requirement</span></span> | <span data-ttu-id="60046-121">Valor</span><span class="sxs-lookup"><span data-stu-id="60046-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60046-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60046-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60046-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="60046-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="60046-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60046-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60046-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="60046-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="60046-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60046-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="60046-127"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="60046-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60046-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="60046-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60046-129">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="60046-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="60046-130">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="60046-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="60046-131">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="60046-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




