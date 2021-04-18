---
description: Retorna o número de processos que têm permissão para abrir recursos compartilhados com acesso restrito.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793365"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a><span data-ttu-id="b81e9-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span><span class="sxs-lookup"><span data-stu-id="b81e9-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span></span>

<span data-ttu-id="b81e9-104">Retorna o número de processos que têm permissão para abrir recursos compartilhados com acesso restrito.</span><span class="sxs-lookup"><span data-stu-id="b81e9-104">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="b81e9-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81e9-105">Requirement</span></span> | <span data-ttu-id="b81e9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b81e9-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e9-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="b81e9-107">Query GUID</span></span>  | <span data-ttu-id="b81e9-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span><span class="sxs-lookup"><span data-stu-id="b81e9-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>                                                                                                |
| <span data-ttu-id="b81e9-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="b81e9-109">Input data</span></span>  | [<span data-ttu-id="b81e9-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b81e9-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                           |
| <span data-ttu-id="b81e9-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="b81e9-111">Return data</span></span> | [<span data-ttu-id="b81e9-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="b81e9-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b81e9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b81e9-113">Remarks</span></span>

<span data-ttu-id="b81e9-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="b81e9-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="b81e9-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="b81e9-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="b81e9-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b81e9-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="b81e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b81e9-117">Requirements</span></span>



| <span data-ttu-id="b81e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81e9-118">Requirement</span></span> | <span data-ttu-id="b81e9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b81e9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b81e9-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b81e9-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b81e9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b81e9-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b81e9-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b81e9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b81e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b81e9-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81e9-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81e9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b81e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81e9-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="b81e9-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b81e9-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="b81e9-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b81e9-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b81e9-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




