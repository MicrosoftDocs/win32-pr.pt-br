---
description: Retorna o tipo de barramento de e/s usado para enviar dados para a GPU.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370532"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="6b94d-103">\_Acessibilidade D3DAUTHENTICATEDQUERY</span><span class="sxs-lookup"><span data-stu-id="6b94d-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="6b94d-104">Retorna o tipo de barramento de e/s usado para enviar dados para a GPU.</span><span class="sxs-lookup"><span data-stu-id="6b94d-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="6b94d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b94d-105">Requirement</span></span> | <span data-ttu-id="6b94d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6b94d-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b94d-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="6b94d-107">Query GUID</span></span>  | <span data-ttu-id="6b94d-108">**\_Acessibilidade D3DAUTHENTICATEDQUERY**</span><span class="sxs-lookup"><span data-stu-id="6b94d-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="6b94d-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="6b94d-109">Input data</span></span>  | [<span data-ttu-id="6b94d-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6b94d-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="6b94d-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="6b94d-111">Return data</span></span> | [<span data-ttu-id="6b94d-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYINFOBUSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="6b94d-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="6b94d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b94d-113">Remarks</span></span>

<span data-ttu-id="6b94d-114">Essa consulta também retorna informações sobre como o conteúdo é acessível quando colocado na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6b94d-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="6b94d-115">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="6b94d-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="6b94d-116">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6b94d-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="6b94d-117">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="6b94d-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="6b94d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b94d-118">Requirements</span></span>



| <span data-ttu-id="6b94d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b94d-119">Requirement</span></span> | <span data-ttu-id="6b94d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6b94d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b94d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b94d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b94d-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6b94d-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b94d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b94d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b94d-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6b94d-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b94d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b94d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b94d-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b94d-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b94d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b94d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b94d-128">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="6b94d-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="6b94d-129">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="6b94d-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6b94d-130">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="6b94d-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




