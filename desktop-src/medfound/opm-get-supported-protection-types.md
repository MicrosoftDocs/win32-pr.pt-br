---
description: Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921214"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="66a76-103">os \_ tipos de proteção de OPM \_ têm suporte \_ \_</span><span class="sxs-lookup"><span data-stu-id="66a76-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="66a76-104">Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.</span><span class="sxs-lookup"><span data-stu-id="66a76-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="66a76-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a76-105">Requirement</span></span> | <span data-ttu-id="66a76-106">Valor</span><span class="sxs-lookup"><span data-stu-id="66a76-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="66a76-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="66a76-107">Request GUID</span></span> | <span data-ttu-id="66a76-108">os \_ tipos de proteção de OPM \_ têm suporte \_ \_</span><span class="sxs-lookup"><span data-stu-id="66a76-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="66a76-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="66a76-109">Input data</span></span>   | <span data-ttu-id="66a76-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="66a76-110">None</span></span>                                                                        |
| <span data-ttu-id="66a76-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="66a76-111">Return data</span></span>  | <span data-ttu-id="66a76-112">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="66a76-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="66a76-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a76-113">Remarks</span></span>

<span data-ttu-id="66a76-114">Os mecanismos de proteção são retornados no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="66a76-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="66a76-115">O valor é um dos sinalizadores de [tipo de proteção](opm-protection-type-flags.md)de bits **ou** de Unificação de OPM.</span><span class="sxs-lookup"><span data-stu-id="66a76-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="66a76-116">Essa consulta é equivalente à consulta DXVA \_ COPPQueryProtectionType usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="66a76-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="66a76-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a76-117">Requirements</span></span>



| <span data-ttu-id="66a76-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a76-118">Requirement</span></span> | <span data-ttu-id="66a76-119">Valor</span><span class="sxs-lookup"><span data-stu-id="66a76-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66a76-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66a76-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66a76-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="66a76-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66a76-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66a76-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66a76-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66a76-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a76-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a76-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a76-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="66a76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a76-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="66a76-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="66a76-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="66a76-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="66a76-129">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="66a76-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




