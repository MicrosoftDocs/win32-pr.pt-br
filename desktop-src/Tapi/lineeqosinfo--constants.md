---
description: Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (qualidade de serviço).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Constantes de LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769404"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="03f65-103">\_Constantes LINEEQOSINFO</span><span class="sxs-lookup"><span data-stu-id="03f65-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="03f65-104">Essas constantes são usadas por um TSP para identificar o resultado de uma solicitação de QoS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="03f65-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="03f65-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**</span><span class="sxs-lookup"><span data-stu-id="03f65-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="03f65-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="03f65-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="03f65-107">A QoS não está disponível.</span><span class="sxs-lookup"><span data-stu-id="03f65-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03f65-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**</span><span class="sxs-lookup"><span data-stu-id="03f65-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="03f65-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="03f65-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="03f65-110">Não foi possível atender à solicitação de QoS.</span><span class="sxs-lookup"><span data-stu-id="03f65-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03f65-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**</span><span class="sxs-lookup"><span data-stu-id="03f65-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="03f65-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="03f65-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="03f65-113">Não há suporte para o tipo de QoS solicitado.</span><span class="sxs-lookup"><span data-stu-id="03f65-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="03f65-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ erro genérico**</span><span class="sxs-lookup"><span data-stu-id="03f65-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="03f65-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="03f65-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="03f65-116">Erro de QoS não especificado.</span><span class="sxs-lookup"><span data-stu-id="03f65-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03f65-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f65-117">Requirements</span></span>



| <span data-ttu-id="03f65-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f65-118">Requirement</span></span> | <span data-ttu-id="03f65-119">Valor</span><span class="sxs-lookup"><span data-stu-id="03f65-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="03f65-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="03f65-120">TAPI version</span></span><br/> | <span data-ttu-id="03f65-121">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="03f65-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="03f65-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03f65-122">Header</span></span><br/>       | <dl> <span data-ttu-id="03f65-123"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f65-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




