---
description: Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646598"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="55854-103">Saída de D3DAUTHENTICATEDQUERY \_</span><span class="sxs-lookup"><span data-stu-id="55854-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="55854-104">Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="55854-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="55854-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="55854-105">Requirement</span></span> | <span data-ttu-id="55854-106">Valor</span><span class="sxs-lookup"><span data-stu-id="55854-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55854-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="55854-107">Query GUID</span></span>  | <span data-ttu-id="55854-108">**Saída de D3DAUTHENTICATEDQUERY \_**</span><span class="sxs-lookup"><span data-stu-id="55854-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="55854-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="55854-109">Input data</span></span>  | [<span data-ttu-id="55854-110">**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**</span><span class="sxs-lookup"><span data-stu-id="55854-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="55854-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="55854-111">Return data</span></span> | [<span data-ttu-id="55854-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**</span><span class="sxs-lookup"><span data-stu-id="55854-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="55854-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55854-113">Remarks</span></span>

<span data-ttu-id="55854-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="55854-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="55854-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="55854-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="55854-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="55854-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="55854-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55854-117">Requirements</span></span>



| <span data-ttu-id="55854-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55854-118">Requirement</span></span> | <span data-ttu-id="55854-119">Valor</span><span class="sxs-lookup"><span data-stu-id="55854-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55854-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55854-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55854-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="55854-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55854-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55854-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55854-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="55854-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55854-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55854-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55854-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="55854-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55854-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="55854-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55854-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="55854-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="55854-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="55854-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="55854-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="55854-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




