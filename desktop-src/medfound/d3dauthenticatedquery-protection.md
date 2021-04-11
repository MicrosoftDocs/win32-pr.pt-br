---
description: Retorna o nível de proteção atual para o dispositivo.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164195"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="a93ba-103">Proteção do D3DAUTHENTICATEDQUERY \_</span><span class="sxs-lookup"><span data-stu-id="a93ba-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="a93ba-104">Retorna o nível de proteção atual para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a93ba-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="a93ba-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93ba-105">Requirement</span></span> | <span data-ttu-id="a93ba-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a93ba-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93ba-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="a93ba-107">Query GUID</span></span>  | <span data-ttu-id="a93ba-108">**Proteção do D3DAUTHENTICATEDQUERY \_**</span><span class="sxs-lookup"><span data-stu-id="a93ba-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="a93ba-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="a93ba-109">Input data</span></span>  | [<span data-ttu-id="a93ba-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="a93ba-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="a93ba-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="a93ba-111">Return data</span></span> | [<span data-ttu-id="a93ba-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYPROTECTION \_**</span><span class="sxs-lookup"><span data-stu-id="a93ba-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="a93ba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a93ba-113">Remarks</span></span>

<span data-ttu-id="a93ba-114">Esta consulta é válida para todos os tipos de canal.</span><span class="sxs-lookup"><span data-stu-id="a93ba-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a93ba-115">Requirements</span></span>



| <span data-ttu-id="a93ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93ba-116">Requirement</span></span> | <span data-ttu-id="a93ba-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a93ba-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a93ba-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a93ba-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a93ba-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a93ba-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a93ba-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a93ba-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a93ba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a93ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a93ba-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a93ba-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93ba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a93ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93ba-125">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="a93ba-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="a93ba-126">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="a93ba-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="a93ba-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a93ba-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




