---
description: Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783216"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="b37e5-103">D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span><span class="sxs-lookup"><span data-stu-id="b37e5-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="b37e5-104">Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.</span><span class="sxs-lookup"><span data-stu-id="b37e5-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="b37e5-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="b37e5-105">Requirement</span></span> | <span data-ttu-id="b37e5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b37e5-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b37e5-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="b37e5-107">Query GUID</span></span>  | <span data-ttu-id="b37e5-108">**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span><span class="sxs-lookup"><span data-stu-id="b37e5-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="b37e5-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="b37e5-109">Input data</span></span>  | [<span data-ttu-id="b37e5-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b37e5-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="b37e5-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="b37e5-111">Return data</span></span> | [<span data-ttu-id="b37e5-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="b37e5-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b37e5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b37e5-113">Remarks</span></span>

<span data-ttu-id="b37e5-114">O único tipo de canal que dá suporte a essa consulta é o **\_ \_ software de driver D3DAUTHENTICATEDCHANNEL**.</span><span class="sxs-lookup"><span data-stu-id="b37e5-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b37e5-115">Requirements</span></span>



| <span data-ttu-id="b37e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b37e5-116">Requirement</span></span> | <span data-ttu-id="b37e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b37e5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b37e5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b37e5-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b37e5-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b37e5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b37e5-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b37e5-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b37e5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b37e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b37e5-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b37e5-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b37e5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b37e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37e5-125">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="b37e5-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b37e5-126">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="b37e5-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b37e5-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b37e5-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




