---
description: Especifica a URL original para um fluxo de bytes.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Atributo MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760107"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="12925-103">\_Atributo de \_ nome de origem MF bytes \_</span><span class="sxs-lookup"><span data-stu-id="12925-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="12925-104">Especifica a URL original para um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="12925-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="12925-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="12925-105">Data type</span></span>

<span data-ttu-id="12925-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="12925-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="12925-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="12925-107">Remarks</span></span>

<span data-ttu-id="12925-108">Os fluxos de bytes baseados em arquivo podem dar suporte a esse atributo.</span><span class="sxs-lookup"><span data-stu-id="12925-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="12925-109">O valor do atributo é definido quando o fluxo de bytes é criado.</span><span class="sxs-lookup"><span data-stu-id="12925-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="12925-110">Para obter o valor do atributo, consulte o objeto de fluxo de bytes para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="12925-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="12925-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="12925-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="12925-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12925-112">Requirements</span></span>



| <span data-ttu-id="12925-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12925-113">Requirement</span></span> | <span data-ttu-id="12925-114">Valor</span><span class="sxs-lookup"><span data-stu-id="12925-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12925-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12925-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12925-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="12925-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="12925-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12925-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12925-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="12925-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="12925-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12925-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="12925-120"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12925-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12925-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="12925-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12925-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12925-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="12925-123">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="12925-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="12925-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="12925-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="12925-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="12925-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="12925-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="12925-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




