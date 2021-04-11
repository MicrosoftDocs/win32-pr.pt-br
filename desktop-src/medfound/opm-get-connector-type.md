---
description: Retorna o tipo de conector físico da saída de vídeo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164904"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="157f6-103">\_tipo de \_ conector de obtenção de OPM \_</span><span class="sxs-lookup"><span data-stu-id="157f6-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="157f6-104">Retorna o tipo de conector físico da saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="157f6-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="157f6-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="157f6-105">Requirement</span></span> | <span data-ttu-id="157f6-106">Valor</span><span class="sxs-lookup"><span data-stu-id="157f6-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="157f6-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="157f6-107">Request GUID</span></span> | <span data-ttu-id="157f6-108">\_tipo de \_ conector de obtenção de OPM \_</span><span class="sxs-lookup"><span data-stu-id="157f6-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="157f6-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="157f6-109">Input data</span></span>   | <span data-ttu-id="157f6-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="157f6-110">None</span></span>                                                                        |
| <span data-ttu-id="157f6-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="157f6-111">Return data</span></span>  | <span data-ttu-id="157f6-112">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="157f6-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="157f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="157f6-113">Remarks</span></span>

<span data-ttu-id="157f6-114">O tipo de conector é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="157f6-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="157f6-115">O valor de **ulInformation** é igual a um dos tipos de conector listados nos [**sinalizadores de tipo de conector OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="157f6-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="157f6-116">No modo de emulação COPP, o tipo de conector pode ser combinado com o sinalizador **interno do tipo de \_ conector OPM Copp \_ compatível \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="157f6-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="157f6-117">Use um **e bit e** para extrair o tipo de conector:</span><span class="sxs-lookup"><span data-stu-id="157f6-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="157f6-118">Os aplicativos devem ignorar o sinalizador **\_ \_ \_ \_ \_ interno do tipo conector compatível com OPM Copp** .</span><span class="sxs-lookup"><span data-stu-id="157f6-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="157f6-119">Para obter mais informações, consulte a seção comentários dos [**sinalizadores de tipo de conector OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="157f6-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="157f6-120">Essa consulta é equivalente à consulta DXVA \_ COPPQueryConnectorType usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="157f6-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="157f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="157f6-121">Requirements</span></span>



| <span data-ttu-id="157f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="157f6-122">Requirement</span></span> | <span data-ttu-id="157f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="157f6-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="157f6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="157f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="157f6-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="157f6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="157f6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="157f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="157f6-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="157f6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="157f6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="157f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="157f6-129"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="157f6-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="157f6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="157f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="157f6-131">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="157f6-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="157f6-132">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="157f6-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="157f6-133">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="157f6-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




