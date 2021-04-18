---
description: Retorna informações sobre um processo que tem permissão para abrir recursos compartilhados com acesso restrito.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815532"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="3cf2d-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS</span><span class="sxs-lookup"><span data-stu-id="3cf2d-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="3cf2d-104">Retorna informações sobre um processo que tem permissão para abrir recursos compartilhados com acesso restrito.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="3cf2d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf2d-105">Requirement</span></span> | <span data-ttu-id="3cf2d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3cf2d-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf2d-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="3cf2d-107">Query GUID</span></span>  | <span data-ttu-id="3cf2d-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="3cf2d-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="3cf2d-109">Input data</span></span>  | [<span data-ttu-id="3cf2d-110">**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="3cf2d-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="3cf2d-111">Return data</span></span> | [<span data-ttu-id="3cf2d-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="3cf2d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cf2d-113">Remarks</span></span>

<span data-ttu-id="3cf2d-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="3cf2d-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="3cf2d-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="3cf2d-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf2d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf2d-117">Requirements</span></span>



| <span data-ttu-id="3cf2d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf2d-118">Requirement</span></span> | <span data-ttu-id="3cf2d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3cf2d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf2d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cf2d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf2d-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3cf2d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3cf2d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cf2d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf2d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3cf2d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3cf2d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cf2d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf2d-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf2d-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf2d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cf2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf2d-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="3cf2d-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="3cf2d-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="3cf2d-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3cf2d-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="3cf2d-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




