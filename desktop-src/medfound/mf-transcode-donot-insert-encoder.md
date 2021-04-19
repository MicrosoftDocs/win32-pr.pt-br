---
description: Especifica se um codificador deve ser incluído na topologia de transcodificação.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Atributo MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764084"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="e2466-103">\_Atributo de \_ \_ \_ CODIFICAdor INSERT não cercamento MF</span><span class="sxs-lookup"><span data-stu-id="e2466-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="e2466-104">Especifica se um codificador deve ser incluído na topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="e2466-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="e2466-105">A função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) verifica esse atributo durante a compilação da topologia.</span><span class="sxs-lookup"><span data-stu-id="e2466-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="e2466-106">Se esse atributo não for definido, um codificador será inserido na topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="e2466-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2466-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e2466-107">Data type</span></span>

<span data-ttu-id="e2466-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2466-108">**UINT32**</span></span>



| <span data-ttu-id="e2466-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e2466-109">Value</span></span>                                                                        | <span data-ttu-id="e2466-110">Significado</span><span class="sxs-lookup"><span data-stu-id="e2466-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2466-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2466-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e2466-112">Um codificador é inserido na topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="e2466-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="e2466-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2466-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e2466-114">Um codificador não está incluído na topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="e2466-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="e2466-115">O nó de origem está conectado ao nó de saída.</span><span class="sxs-lookup"><span data-stu-id="e2466-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2466-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2466-116">Remarks</span></span>

<span data-ttu-id="e2466-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e2466-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2466-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2466-118">Requirements</span></span>



| <span data-ttu-id="e2466-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2466-119">Requirement</span></span> | <span data-ttu-id="e2466-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e2466-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2466-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2466-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2466-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e2466-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2466-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2466-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2466-124">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e2466-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e2466-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2466-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2466-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2466-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2466-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2466-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2466-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2466-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2466-129">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2466-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




