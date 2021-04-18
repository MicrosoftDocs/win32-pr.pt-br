---
description: Define o nível de proteção para um mecanismo de proteção de saída.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791357"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="3674a-103">OPM \_ definir \_ nível de proteção \_</span><span class="sxs-lookup"><span data-stu-id="3674a-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="3674a-104">Define o nível de proteção para um mecanismo de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="3674a-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="3674a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3674a-105">Requirement</span></span> | <span data-ttu-id="3674a-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3674a-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3674a-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="3674a-107">Command GUID</span></span> | <span data-ttu-id="3674a-108">OPM \_ definir \_ nível de proteção \_</span><span class="sxs-lookup"><span data-stu-id="3674a-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="3674a-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="3674a-109">Input data</span></span>   | <span data-ttu-id="3674a-110">Uma estrutura de [**parâmetros de nível de proteção dos OPMS \_ definidos \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="3674a-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3674a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3674a-111">Remarks</span></span>

<span data-ttu-id="3674a-112">Alguns conectores podem dar suporte a vários mecanismos de proteção.</span><span class="sxs-lookup"><span data-stu-id="3674a-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="3674a-113">Com esse tipo de conector, você pode aplicar vários mecanismos de proteção ao mesmo conector, com configurações diferentes para cada um.</span><span class="sxs-lookup"><span data-stu-id="3674a-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="3674a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3674a-114">Requirements</span></span>



| <span data-ttu-id="3674a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3674a-115">Requirement</span></span> | <span data-ttu-id="3674a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3674a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3674a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3674a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3674a-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3674a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3674a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3674a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3674a-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3674a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3674a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3674a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3674a-122"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3674a-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3674a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3674a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3674a-124">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="3674a-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="3674a-125">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="3674a-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




