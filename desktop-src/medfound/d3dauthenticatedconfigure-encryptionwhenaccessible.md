---
description: Define o nível de criptografia que é executado antes que o conteúdo protegido se torne acessível à CPU ou ao barramento.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501185"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="8f72b-103">D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="8f72b-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="8f72b-104">Define o nível de criptografia que é executado antes que o conteúdo protegido se torne acessível à CPU ou ao barramento.</span><span class="sxs-lookup"><span data-stu-id="8f72b-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="8f72b-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f72b-105">Requirement</span></span> | <span data-ttu-id="8f72b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8f72b-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f72b-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="8f72b-107">Command GUID</span></span> | <span data-ttu-id="8f72b-108">**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="8f72b-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="8f72b-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="8f72b-109">Input data</span></span>   | [<span data-ttu-id="8f72b-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**</span><span class="sxs-lookup"><span data-stu-id="8f72b-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="8f72b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f72b-111">Remarks</span></span>

<span data-ttu-id="8f72b-112">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="8f72b-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="8f72b-113">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8f72b-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="8f72b-114">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="8f72b-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8f72b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f72b-115">Requirements</span></span>



| <span data-ttu-id="8f72b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f72b-116">Requirement</span></span> | <span data-ttu-id="8f72b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8f72b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f72b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f72b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8f72b-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8f72b-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8f72b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f72b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8f72b-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8f72b-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8f72b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f72b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f72b-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f72b-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f72b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f72b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f72b-125">Comandos de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="8f72b-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="8f72b-126">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="8f72b-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8f72b-127">**IDirect3DAuthenticatedChannel9:: configurar**</span><span class="sxs-lookup"><span data-stu-id="8f72b-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




