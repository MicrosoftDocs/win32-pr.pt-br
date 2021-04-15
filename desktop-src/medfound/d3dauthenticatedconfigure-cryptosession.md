---
description: Associa uma sessão criptográfica a um dispositivo decodificador do DirectX Video Acceleration 2 (DXVA-2) e a um dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753843"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="e6de0-103">D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="e6de0-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="e6de0-104">Associa uma sessão criptográfica a um dispositivo decodificador do DirectX Video Acceleration 2 (DXVA-2) e a um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e6de0-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="e6de0-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6de0-105">Requirement</span></span> | <span data-ttu-id="e6de0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e6de0-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6de0-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="e6de0-107">Command GUID</span></span> | <span data-ttu-id="e6de0-108">**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="e6de0-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="e6de0-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="e6de0-109">Input data</span></span>   | [<span data-ttu-id="e6de0-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="e6de0-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="e6de0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6de0-111">Remarks</span></span>

<span data-ttu-id="e6de0-112">Depois que esse comando for enviado, você poderá enviar a consulta [D3DAUTHENTICATEDQUERY \_ outputid](d3dauthenticatedquery-outputid.md) para descobrir quais saídas de vídeo estão associadas à sessão criptográfica.</span><span class="sxs-lookup"><span data-stu-id="e6de0-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="e6de0-113">Os seguintes tipos de canal dão suporte a este comando:</span><span class="sxs-lookup"><span data-stu-id="e6de0-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="e6de0-114">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="e6de0-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="e6de0-115">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="e6de0-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="e6de0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6de0-116">Requirements</span></span>



| <span data-ttu-id="e6de0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6de0-117">Requirement</span></span> | <span data-ttu-id="e6de0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e6de0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6de0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6de0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6de0-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6de0-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6de0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6de0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6de0-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e6de0-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6de0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6de0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6de0-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6de0-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6de0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6de0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6de0-126">Comandos de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="e6de0-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="e6de0-127">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="e6de0-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e6de0-128">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="e6de0-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




