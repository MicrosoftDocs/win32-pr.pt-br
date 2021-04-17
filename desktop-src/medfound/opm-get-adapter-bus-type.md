---
description: Retorna o tipo de barramento de e/s usado pela saída de vídeo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791367"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="a80df-103">\_tipo de \_ barramento de adaptador de obtenção de OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="a80df-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="a80df-104">Retorna o tipo de barramento de e/s usado pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a80df-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="a80df-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80df-105">Requirement</span></span> | <span data-ttu-id="a80df-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a80df-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a80df-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="a80df-107">Request GUID</span></span> | <span data-ttu-id="a80df-108">\_tipo de \_ barramento de adaptador de obtenção de OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="a80df-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="a80df-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="a80df-109">Input data</span></span>   | <span data-ttu-id="a80df-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a80df-110">None</span></span>                                                                        |
| <span data-ttu-id="a80df-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="a80df-111">Return data</span></span>  | <span data-ttu-id="a80df-112">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="a80df-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a80df-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a80df-113">Remarks</span></span>

<span data-ttu-id="a80df-114">O tipo de barramento é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="a80df-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="a80df-115">O valor é um dos sinalizadores de [**tipo de barramento**](opm-bus-type-flags.md)de bits **ou** unibit de OPM.</span><span class="sxs-lookup"><span data-stu-id="a80df-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="a80df-116">Essa consulta é equivalente à consulta DXVA \_ COPPQueryBusData usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="a80df-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="a80df-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80df-117">Requirements</span></span>



| <span data-ttu-id="a80df-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80df-118">Requirement</span></span> | <span data-ttu-id="a80df-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a80df-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a80df-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a80df-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a80df-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a80df-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a80df-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a80df-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a80df-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a80df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80df-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a80df-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a80df-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a80df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80df-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="a80df-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="a80df-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="a80df-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="a80df-129">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="a80df-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




