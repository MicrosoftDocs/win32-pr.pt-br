---
description: Especifica informações sobre o sinal de vídeo, além do nível de proteção.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502263"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="8bb65-103">OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_</span><span class="sxs-lookup"><span data-stu-id="8bb65-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="8bb65-104">Especifica informações sobre o sinal de vídeo, além do nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="8bb65-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="8bb65-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb65-105">Requirement</span></span> | <span data-ttu-id="8bb65-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb65-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb65-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="8bb65-107">Command GUID</span></span> | <span data-ttu-id="8bb65-108">OPM \_ define \_ a \_ \_ sinalização ACP e CGMSA \_</span><span class="sxs-lookup"><span data-stu-id="8bb65-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="8bb65-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="8bb65-109">Input data</span></span>   | <span data-ttu-id="8bb65-110">Uma estrutura de [**\_ \_ \_ \_ \_ \_ parâmetros de sinalização de CGMSA**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) de dados de configuração de um OPM</span><span class="sxs-lookup"><span data-stu-id="8bb65-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8bb65-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bb65-111">Remarks</span></span>

<span data-ttu-id="8bb65-112">Esse comando é equivalente ao comando DXVA \_ COPPSetSignaling usado no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="8bb65-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="8bb65-113">Para o CGMS-A, determinados padrões de proteção exigem que o sinal de televisão contenha informações dentro dos mesmos pacotes VBI de forma de onda que os bits CGMS-A.</span><span class="sxs-lookup"><span data-stu-id="8bb65-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="8bb65-114">Entre outras coisas, essas informações incluem a taxa de proporção da imagem.</span><span class="sxs-lookup"><span data-stu-id="8bb65-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="8bb65-115">As televisões podem exibir inadequadamente se as informações de taxa de proporção não estiverem consistentes com o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8bb65-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="8bb65-116">O aplicativo pode usar esse comando para especificar a taxa de proporção para que o driver de gráficos possa gerar os pacotes VBI corretos.</span><span class="sxs-lookup"><span data-stu-id="8bb65-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb65-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb65-117">Requirements</span></span>



| <span data-ttu-id="8bb65-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb65-118">Requirement</span></span> | <span data-ttu-id="8bb65-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8bb65-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb65-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bb65-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb65-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bb65-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8bb65-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bb65-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb65-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8bb65-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8bb65-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8bb65-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb65-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb65-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb65-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bb65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb65-127">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="8bb65-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="8bb65-128">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="8bb65-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




