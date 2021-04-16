---
description: Especifica se uma Media Foundation de transformação (MFT) dá suporte a alterações de formato dinâmico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Atributo MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773019"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="6c787-103">MFT \_ dá suporte ao \_ \_ atributo de alteração de formato dinâmico \_</span><span class="sxs-lookup"><span data-stu-id="6c787-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="6c787-104">Especifica se uma Media Foundation de transformação (MFT) dá suporte a alterações de formato dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6c787-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c787-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6c787-105">Data type</span></span>

<span data-ttu-id="6c787-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6c787-106">**UINT32**</span></span>

<span data-ttu-id="6c787-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="6c787-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c787-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c787-108">Remarks</span></span>

<span data-ttu-id="6c787-109">Esse atributo pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c787-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="6c787-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6c787-110">Value</span></span>     | <span data-ttu-id="6c787-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c787-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="6c787-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6c787-112">**TRUE**</span></span>  | <span data-ttu-id="6c787-113">O cliente pode alterar o formato de entrada durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="6c787-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="6c787-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="6c787-114">**FALSE**</span></span> | <span data-ttu-id="6c787-115">A MFT deve ser descarregada antes que o cliente possa alterar o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c787-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="6c787-116">Para obter esse atributo, primeiro chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global para o MFT.</span><span class="sxs-lookup"><span data-stu-id="6c787-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="6c787-117">Em seguida, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="6c787-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="6c787-118">Se [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) falhar ou o atributo não estiver presente, o valor padrão se for **false**.</span><span class="sxs-lookup"><span data-stu-id="6c787-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="6c787-119">O [MFTs assíncrono](asynchronous-mfts.md) deve retornar o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="6c787-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="6c787-120">Para obter mais informações, consulte [lidando com alterações de fluxo](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="6c787-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="6c787-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6c787-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c787-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c787-122">Requirements</span></span>



| <span data-ttu-id="6c787-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c787-123">Requirement</span></span> | <span data-ttu-id="6c787-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6c787-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c787-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c787-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6c787-126">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c787-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6c787-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c787-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6c787-128">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6c787-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6c787-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c787-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c787-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c787-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c787-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c787-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c787-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6c787-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c787-133">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="6c787-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="6c787-134">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="6c787-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c787-135">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6c787-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6c787-136">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="6c787-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6c787-137">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6c787-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




