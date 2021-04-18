---
description: Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787713"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="6c267-103">OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c267-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="6c267-104">Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6c267-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="6c267-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c267-105">Requirement</span></span> | <span data-ttu-id="6c267-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6c267-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6c267-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="6c267-107">Request GUID</span></span> | <span data-ttu-id="6c267-108">OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c267-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="6c267-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="6c267-109">Input data</span></span>   | <span data-ttu-id="6c267-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6c267-110">None</span></span>                                                                        |
| <span data-ttu-id="6c267-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="6c267-111">Return data</span></span>  | <span data-ttu-id="6c267-112">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="6c267-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c267-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c267-113">Remarks</span></span>

<span data-ttu-id="6c267-114">Se essa consulta for realizada com sucesso, o membro **ulInformation** da estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contém o número de versão do SRM, no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="6c267-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="6c267-115">SRMs são usados para atualizar a lista de dispositivos de High-Bandwidth digital Proteção de Conteúdo (HDCP) revogados.</span><span class="sxs-lookup"><span data-stu-id="6c267-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="6c267-116">SRMs são entregues com o conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6c267-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="6c267-117">Para definir o SRM, envie o comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="6c267-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="6c267-118">Essa consulta pode fazer com que o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retorne qualquer um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c267-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="6c267-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6c267-119">Return code</span></span>                                            | <span data-ttu-id="6c267-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c267-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="6c267-121">gráfico de erros \_ \_ OPM de HDCP do \_ \_ SRM \_ nunca \_ definido</span><span class="sxs-lookup"><span data-stu-id="6c267-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="6c267-122">O aplicativo não definiu um SRM.</span><span class="sxs-lookup"><span data-stu-id="6c267-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="6c267-123">ERRO \_ gráficos \_ de \_ saída \_ OPM \_ não \_ dá suporte a \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="6c267-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="6c267-124">A saída de vídeo não oferece suporte a HDCP.</span><span class="sxs-lookup"><span data-stu-id="6c267-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6c267-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c267-125">Requirements</span></span>



| <span data-ttu-id="6c267-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c267-126">Requirement</span></span> | <span data-ttu-id="6c267-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6c267-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c267-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c267-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c267-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c267-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6c267-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c267-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c267-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c267-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c267-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c267-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c267-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c267-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c267-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c267-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c267-135">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="6c267-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="6c267-136">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="6c267-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




