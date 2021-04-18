---
description: Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796168"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="0c154-103">\_ID de \_ saída de obtenção de OPM \_</span><span class="sxs-lookup"><span data-stu-id="0c154-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="0c154-104">Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0c154-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="0c154-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c154-105">Requirement</span></span> | <span data-ttu-id="0c154-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0c154-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="0c154-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="0c154-107">Request GUID</span></span> | <span data-ttu-id="0c154-108">\_ID de \_ saída de obtenção de OPM \_</span><span class="sxs-lookup"><span data-stu-id="0c154-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="0c154-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="0c154-109">Input data</span></span>   | <span data-ttu-id="0c154-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0c154-110">None</span></span>                                                             |
| <span data-ttu-id="0c154-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="0c154-111">Return data</span></span>  | <span data-ttu-id="0c154-112">Uma estrutura de [**\_ dados de \_ ID \_ de saída OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)</span><span class="sxs-lookup"><span data-stu-id="0c154-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0c154-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c154-113">Remarks</span></span>

<span data-ttu-id="0c154-114">O driver de vídeo atribui um identificador exclusivo a cada monitor.</span><span class="sxs-lookup"><span data-stu-id="0c154-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="0c154-115">Essa consulta retorna o identificador do monitor que está associado ao ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) atual.</span><span class="sxs-lookup"><span data-stu-id="0c154-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c154-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c154-116">Requirements</span></span>



| <span data-ttu-id="0c154-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c154-117">Requirement</span></span> | <span data-ttu-id="0c154-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0c154-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0c154-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c154-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0c154-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c154-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0c154-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c154-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0c154-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c154-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0c154-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c154-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c154-124"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c154-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c154-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c154-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c154-126">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="0c154-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="0c154-127">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="0c154-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




