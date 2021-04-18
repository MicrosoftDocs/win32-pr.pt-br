---
description: Inicializa o canal autenticado.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788862"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="8b9f2-103">D3DAUTHENTICATEDCONFIGURE \_ inicializar</span><span class="sxs-lookup"><span data-stu-id="8b9f2-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="8b9f2-104">Inicializa o canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="8b9f2-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="8b9f2-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9f2-105">Requirement</span></span> | <span data-ttu-id="8b9f2-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8b9f2-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9f2-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="8b9f2-107">Command GUID</span></span> | <span data-ttu-id="8b9f2-108">**D3DAUTHENTICATEDCONFIGURE \_ inicializar**</span><span class="sxs-lookup"><span data-stu-id="8b9f2-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="8b9f2-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="8b9f2-109">Input data</span></span>   | [<span data-ttu-id="8b9f2-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="8b9f2-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="8b9f2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b9f2-111">Remarks</span></span>

<span data-ttu-id="8b9f2-112">Envie este comando uma vez, no início da sessão.</span><span class="sxs-lookup"><span data-stu-id="8b9f2-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="8b9f2-113">Esse comando só pode ser enviado uma vez para cada canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="8b9f2-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="8b9f2-114">O número de sequência de entrada é ignorado para esse comando.</span><span class="sxs-lookup"><span data-stu-id="8b9f2-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="8b9f2-115">Os seguintes tipos de canal dão suporte a este comando:</span><span class="sxs-lookup"><span data-stu-id="8b9f2-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="8b9f2-116">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8b9f2-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="8b9f2-117">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8b9f2-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9f2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b9f2-118">Requirements</span></span>



| <span data-ttu-id="8b9f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b9f2-119">Requirement</span></span> | <span data-ttu-id="8b9f2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8b9f2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9f2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b9f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b9f2-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8b9f2-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8b9f2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b9f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b9f2-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8b9f2-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8b9f2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b9f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b9f2-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b9f2-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9f2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b9f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9f2-128">Comandos de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="8b9f2-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="8b9f2-129">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="8b9f2-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8b9f2-130">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="8b9f2-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




