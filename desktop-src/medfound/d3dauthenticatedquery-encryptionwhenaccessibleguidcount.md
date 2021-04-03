---
description: Retorna o número de tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646599"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="e231e-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="e231e-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="e231e-104">Retorna o número de tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.</span><span class="sxs-lookup"><span data-stu-id="e231e-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="e231e-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e231e-105">Requirement</span></span> | <span data-ttu-id="e231e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e231e-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e231e-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="e231e-107">Query GUID</span></span>  | <span data-ttu-id="e231e-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="e231e-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="e231e-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="e231e-109">Input data</span></span>  | [<span data-ttu-id="e231e-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e231e-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="e231e-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="e231e-111">Return data</span></span> | [<span data-ttu-id="e231e-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**</span><span class="sxs-lookup"><span data-stu-id="e231e-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="e231e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e231e-113">Remarks</span></span>

<span data-ttu-id="e231e-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="e231e-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="e231e-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e231e-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="e231e-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e231e-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="e231e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e231e-117">Requirements</span></span>



| <span data-ttu-id="e231e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e231e-118">Requirement</span></span> | <span data-ttu-id="e231e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e231e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e231e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e231e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e231e-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e231e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e231e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e231e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e231e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e231e-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e231e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e231e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e231e-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e231e-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e231e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e231e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e231e-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="e231e-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="e231e-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="e231e-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e231e-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="e231e-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




