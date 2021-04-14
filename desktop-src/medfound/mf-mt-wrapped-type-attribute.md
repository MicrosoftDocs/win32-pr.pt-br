---
description: Contém um tipo de mídia que foi encapsulado em outro tipo de mídia.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Atributo MF_MT_WRAPPED_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370520"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="5e9a7-103">\_Atributo de \_ tipo empacotado MF MT \_</span><span class="sxs-lookup"><span data-stu-id="5e9a7-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="5e9a7-104">Contém um tipo de mídia que foi encapsulado em outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e9a7-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5e9a7-105">Data type</span></span>

<span data-ttu-id="5e9a7-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="5e9a7-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9a7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e9a7-107">Remarks</span></span>

<span data-ttu-id="5e9a7-108">Esse atributo é usado na função [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , que encapsula um tipo de mídia dentro de outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="5e9a7-109">A função [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e9a7-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="5e9a7-110">Converte o tipo de mídia original em uma matriz binária.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="5e9a7-111">Define o atributo de **\_ \_ \_ tipo empacotado MF MT** no novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="5e9a7-112">O valor do atributo é a matriz binária.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="5e9a7-113">Normalmente, os aplicativos não usam esse atributo diretamente.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="5e9a7-114">Para desencapsular o tipo de mídia original, chame [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="5e9a7-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="5e9a7-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9a7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9a7-116">Requirements</span></span>



| <span data-ttu-id="5e9a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9a7-117">Requirement</span></span> | <span data-ttu-id="5e9a7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5e9a7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9a7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e9a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9a7-120">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e9a7-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5e9a7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e9a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9a7-122">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e9a7-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5e9a7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e9a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e9a7-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9a7-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9a7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e9a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9a7-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e9a7-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e9a7-127">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="5e9a7-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5e9a7-128">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="5e9a7-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5e9a7-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5e9a7-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5e9a7-130">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="5e9a7-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




