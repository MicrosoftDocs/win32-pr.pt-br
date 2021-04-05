---
description: Retorna o número de identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646597"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="5bb26-103">D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="5bb26-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="5bb26-104">Retorna o número de identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5bb26-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="5bb26-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb26-105">Requirement</span></span> | <span data-ttu-id="5bb26-106">Valor</span><span class="sxs-lookup"><span data-stu-id="5bb26-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb26-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="5bb26-107">Query GUID</span></span>  | <span data-ttu-id="5bb26-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="5bb26-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="5bb26-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="5bb26-109">Input data</span></span>  | [<span data-ttu-id="5bb26-110">**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="5bb26-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="5bb26-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="5bb26-111">Return data</span></span> | [<span data-ttu-id="5bb26-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="5bb26-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="5bb26-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bb26-113">Remarks</span></span>

<span data-ttu-id="5bb26-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="5bb26-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="5bb26-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="5bb26-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="5bb26-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="5bb26-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb26-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb26-117">Requirements</span></span>



| <span data-ttu-id="5bb26-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb26-118">Requirement</span></span> | <span data-ttu-id="5bb26-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5bb26-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb26-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb26-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb26-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5bb26-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5bb26-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb26-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb26-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5bb26-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5bb26-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bb26-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bb26-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb26-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb26-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bb26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb26-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="5bb26-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="5bb26-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="5bb26-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="5bb26-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="5bb26-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




