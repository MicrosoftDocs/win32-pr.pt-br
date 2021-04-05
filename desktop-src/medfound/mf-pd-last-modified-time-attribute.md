---
description: Especifica quando uma apresentação foi modificada pela última vez.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: Atributo MF_PD_LAST_MODIFIED_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922072"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="69ec6-103">\_Atributo de \_ hora da última \_ modificação \_ do MF PD</span><span class="sxs-lookup"><span data-stu-id="69ec6-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="69ec6-104">Especifica quando uma apresentação foi modificada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="69ec6-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="69ec6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="69ec6-105">Data type</span></span>

<span data-ttu-id="69ec6-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="69ec6-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="69ec6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ec6-107">Remarks</span></span>

<span data-ttu-id="69ec6-108">As fontes de mídia podem definir esse atributo em um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="69ec6-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="69ec6-109">O valor do atributo é uma estrutura **FILETIME** , que é documentada na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="69ec6-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="69ec6-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="69ec6-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ec6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ec6-111">Requirements</span></span>



| <span data-ttu-id="69ec6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ec6-112">Requirement</span></span> | <span data-ttu-id="69ec6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="69ec6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69ec6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ec6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="69ec6-115">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="69ec6-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="69ec6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ec6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="69ec6-117">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69ec6-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69ec6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69ec6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="69ec6-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ec6-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ec6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ec6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ec6-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69ec6-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69ec6-122">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="69ec6-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="69ec6-123">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="69ec6-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="69ec6-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="69ec6-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="69ec6-125">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="69ec6-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




