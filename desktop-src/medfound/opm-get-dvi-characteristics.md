---
description: Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010661"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="5c2d1-103">OPM \_ obter \_ características de DVI \_</span><span class="sxs-lookup"><span data-stu-id="5c2d1-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="5c2d1-104">Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5c2d1-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="5c2d1-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2d1-105">Requirement</span></span> | <span data-ttu-id="5c2d1-106">Valor</span><span class="sxs-lookup"><span data-stu-id="5c2d1-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5c2d1-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="5c2d1-107">Request GUID</span></span> | <span data-ttu-id="5c2d1-108">OPM \_ obter \_ características de DVI \_</span><span class="sxs-lookup"><span data-stu-id="5c2d1-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="5c2d1-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="5c2d1-109">Input data</span></span>   | <span data-ttu-id="5c2d1-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5c2d1-110">None</span></span>                                                                        |
| <span data-ttu-id="5c2d1-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="5c2d1-111">Return data</span></span>  | <span data-ttu-id="5c2d1-112">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="5c2d1-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5c2d1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c2d1-113">Remarks</span></span>

<span data-ttu-id="5c2d1-114">Se essa consulta for realizada com sucesso, o membro **ulInformation** da estrutura de [**\_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c2d1-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="5c2d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5c2d1-115">Value</span></span>                                     | <span data-ttu-id="5c2d1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c2d1-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="5c2d1-117">Característica de DVI de OPM \_ \_ \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c2d1-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="5c2d1-118">DVI versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="5c2d1-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="5c2d1-119">\_Característica DVI de OPM \_ \_ 1 \_ 1 \_ ou \_ acima</span><span class="sxs-lookup"><span data-stu-id="5c2d1-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="5c2d1-120">DVI versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5c2d1-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="5c2d1-121">Essa consulta só tem suporte quando o tipo de conector físico é um tipo de conector de OPM \_ \_ \_ DVI.</span><span class="sxs-lookup"><span data-stu-id="5c2d1-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="5c2d1-122">Para obter o tipo de conector, envie a consulta de [**\_ \_ \_ tipo de conector do OPM**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2d1-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2d1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c2d1-123">Requirements</span></span>



| <span data-ttu-id="5c2d1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2d1-124">Requirement</span></span> | <span data-ttu-id="5c2d1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5c2d1-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2d1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c2d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2d1-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c2d1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5c2d1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c2d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2d1-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c2d1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c2d1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c2d1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2d1-131"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d1-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2d1-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c2d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2d1-133">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="5c2d1-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="5c2d1-134">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="5c2d1-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




