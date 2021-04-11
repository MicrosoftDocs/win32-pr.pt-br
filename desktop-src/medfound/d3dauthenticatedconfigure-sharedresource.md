---
description: Permite que um processo Abra um recurso compartilhado ou desabilite um processo de abrir recursos compartilhados.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164199"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="7ed36-103">D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="7ed36-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="7ed36-104">Permite que um processo Abra um recurso compartilhado ou desabilite um processo de abrir recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="7ed36-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="7ed36-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed36-105">Requirement</span></span> | <span data-ttu-id="7ed36-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7ed36-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed36-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="7ed36-107">Command GUID</span></span> | <span data-ttu-id="7ed36-108">**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="7ed36-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="7ed36-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="7ed36-109">Input data</span></span>   | [<span data-ttu-id="7ed36-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="7ed36-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="7ed36-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ed36-111">Remarks</span></span>

<span data-ttu-id="7ed36-112">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="7ed36-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="7ed36-113">**D3DAUTHENTICATEDCHANNEL \_ Driver \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="7ed36-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="7ed36-114">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="7ed36-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed36-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ed36-115">Requirements</span></span>



| <span data-ttu-id="7ed36-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed36-116">Requirement</span></span> | <span data-ttu-id="7ed36-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7ed36-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed36-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ed36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed36-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7ed36-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7ed36-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ed36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed36-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="7ed36-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7ed36-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ed36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed36-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ed36-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed36-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ed36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed36-125">Comandos de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="7ed36-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="7ed36-126">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="7ed36-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="7ed36-127">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="7ed36-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




