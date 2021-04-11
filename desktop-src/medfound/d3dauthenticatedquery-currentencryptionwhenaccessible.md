---
description: Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível à CPU ou ao barramento.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164198"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="96c5e-103">D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="96c5e-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="96c5e-104">Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível à CPU ou ao barramento.</span><span class="sxs-lookup"><span data-stu-id="96c5e-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="96c5e-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c5e-105">Requirement</span></span> | <span data-ttu-id="96c5e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="96c5e-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c5e-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="96c5e-107">Query GUID</span></span>  | <span data-ttu-id="96c5e-108">**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="96c5e-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="96c5e-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="96c5e-109">Input data</span></span>  | [<span data-ttu-id="96c5e-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="96c5e-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="96c5e-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="96c5e-111">Return data</span></span> | [<span data-ttu-id="96c5e-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**</span><span class="sxs-lookup"><span data-stu-id="96c5e-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="96c5e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="96c5e-113">Remarks</span></span>

<span data-ttu-id="96c5e-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="96c5e-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="96c5e-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="96c5e-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="96c5e-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="96c5e-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="96c5e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c5e-117">Requirements</span></span>



| <span data-ttu-id="96c5e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c5e-118">Requirement</span></span> | <span data-ttu-id="96c5e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="96c5e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c5e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c5e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96c5e-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="96c5e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="96c5e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c5e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96c5e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="96c5e-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="96c5e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96c5e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c5e-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c5e-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c5e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="96c5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c5e-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="96c5e-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="96c5e-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="96c5e-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="96c5e-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="96c5e-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




