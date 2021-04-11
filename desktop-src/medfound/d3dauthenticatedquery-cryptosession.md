---
description: Retorna identificadores para a sessão de criptografia e para o dispositivo Direct3D que estão associados a um dispositivo de decodificador de vídeo do DirectX 2 (DXVA-2) especificado.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164197"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="b2f49-103">D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="b2f49-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="b2f49-104">Retorna identificadores para a sessão de criptografia e para o dispositivo Direct3D que estão associados a um dispositivo de decodificador de vídeo do DirectX 2 (DXVA-2) especificado.</span><span class="sxs-lookup"><span data-stu-id="b2f49-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="b2f49-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f49-105">Requirement</span></span> | <span data-ttu-id="b2f49-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b2f49-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f49-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="b2f49-107">Query GUID</span></span>  | <span data-ttu-id="b2f49-108">**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="b2f49-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="b2f49-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="b2f49-109">Input data</span></span>  | [<span data-ttu-id="b2f49-110">**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b2f49-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="b2f49-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="b2f49-111">Return data</span></span> | [<span data-ttu-id="b2f49-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYCRYPTOSESSION \_**</span><span class="sxs-lookup"><span data-stu-id="b2f49-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="b2f49-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2f49-113">Remarks</span></span>

<span data-ttu-id="b2f49-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="b2f49-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="b2f49-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b2f49-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="b2f49-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b2f49-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f49-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2f49-117">Requirements</span></span>



| <span data-ttu-id="b2f49-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f49-118">Requirement</span></span> | <span data-ttu-id="b2f49-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b2f49-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f49-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2f49-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f49-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b2f49-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b2f49-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2f49-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f49-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b2f49-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2f49-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2f49-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f49-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f49-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f49-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2f49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f49-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="b2f49-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="b2f49-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="b2f49-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b2f49-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="b2f49-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




