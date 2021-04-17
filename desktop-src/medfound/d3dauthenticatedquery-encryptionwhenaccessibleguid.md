---
description: Retorna um dos tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770573"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="75ccd-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID</span><span class="sxs-lookup"><span data-stu-id="75ccd-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="75ccd-104">Retorna um dos tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.</span><span class="sxs-lookup"><span data-stu-id="75ccd-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="75ccd-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ccd-105">Requirement</span></span> | <span data-ttu-id="75ccd-106">Valor</span><span class="sxs-lookup"><span data-stu-id="75ccd-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ccd-107">GUID de consulta</span><span class="sxs-lookup"><span data-stu-id="75ccd-107">Query GUID</span></span>  | <span data-ttu-id="75ccd-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**</span><span class="sxs-lookup"><span data-stu-id="75ccd-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="75ccd-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="75ccd-109">Input data</span></span>  | [<span data-ttu-id="75ccd-110">**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**</span><span class="sxs-lookup"><span data-stu-id="75ccd-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="75ccd-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="75ccd-111">Return data</span></span> | [<span data-ttu-id="75ccd-112">**\_Saída D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**</span><span class="sxs-lookup"><span data-stu-id="75ccd-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="75ccd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="75ccd-113">Remarks</span></span>

<span data-ttu-id="75ccd-114">Os seguintes tipos de canal dão suporte a esta consulta:</span><span class="sxs-lookup"><span data-stu-id="75ccd-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="75ccd-115">**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="75ccd-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="75ccd-116">**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="75ccd-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="75ccd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ccd-117">Requirements</span></span>



| <span data-ttu-id="75ccd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ccd-118">Requirement</span></span> | <span data-ttu-id="75ccd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="75ccd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ccd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75ccd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75ccd-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="75ccd-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="75ccd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75ccd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75ccd-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="75ccd-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="75ccd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ccd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ccd-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ccd-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ccd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="75ccd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ccd-127">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="75ccd-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="75ccd-128">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="75ccd-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="75ccd-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="75ccd-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




