---
description: Retorna um identificador para o dispositivo que está associado a este canal autenticado.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761165"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="03288-103">D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE</span><span class="sxs-lookup"><span data-stu-id="03288-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="03288-104">Retorna um identificador para o dispositivo que está associado a este canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="03288-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="03288-105">Você pode usar esse identificador para verificar se dois canais autenticados estão se comunicando com o mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03288-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="03288-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="03288-106">Requirement</span></span> | <span data-ttu-id="03288-107">Valor</span><span class="sxs-lookup"><span data-stu-id="03288-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03288-108">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="03288-108">Query GUID</span></span>  | <span data-ttu-id="03288-109">**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="03288-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="03288-110">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="03288-110">Input data</span></span>  | [<span data-ttu-id="03288-111">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="03288-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="03288-112">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="03288-112">Return data</span></span> | [<span data-ttu-id="03288-113">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYDEVICEHANDLE \_**</span><span class="sxs-lookup"><span data-stu-id="03288-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="03288-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="03288-114">Remarks</span></span>

<span data-ttu-id="03288-115">Esta consulta é válida para todos os tipos de canal.</span><span class="sxs-lookup"><span data-stu-id="03288-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="03288-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03288-116">Requirements</span></span>



| <span data-ttu-id="03288-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="03288-117">Requirement</span></span> | <span data-ttu-id="03288-118">Valor</span><span class="sxs-lookup"><span data-stu-id="03288-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03288-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03288-119">Minimum supported client</span></span><br/> | <span data-ttu-id="03288-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="03288-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03288-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03288-121">Minimum supported server</span></span><br/> | <span data-ttu-id="03288-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="03288-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03288-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03288-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="03288-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="03288-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03288-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="03288-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03288-126">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="03288-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="03288-127">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="03288-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="03288-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="03288-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




