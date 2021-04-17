---
description: Especifica a duração de um fluxo de bytes, em unidades de 100 a nanossegundos.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: Atributo MF_BYTESTREAM_DURATION (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296566"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="36f49-103">Atributo de duração de \_ bytes MF \_</span><span class="sxs-lookup"><span data-stu-id="36f49-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="36f49-104">Especifica a duração de um fluxo de bytes, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="36f49-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="36f49-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="36f49-105">Data type</span></span>

<span data-ttu-id="36f49-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="36f49-106">**UINT64**</span></span>

<span data-ttu-id="36f49-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="36f49-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36f49-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="36f49-108">Remarks</span></span>

<span data-ttu-id="36f49-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="36f49-109">This attribute is optional.</span></span> <span data-ttu-id="36f49-110">Se o objeto que cria o fluxo de bytes puder determinar a duração, ele poderá definir esse atributo.</span><span class="sxs-lookup"><span data-stu-id="36f49-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="36f49-111">(Por exemplo, em um fluxo de rede, a duração pode ser parte da descrição da sessão.)</span><span class="sxs-lookup"><span data-stu-id="36f49-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="36f49-112">Para obter o valor do atributo, chame **QueryInterface** no fluxo de bytes para obter um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="36f49-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="36f49-113">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="36f49-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="36f49-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="36f49-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f49-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f49-115">Requirements</span></span>



| <span data-ttu-id="36f49-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f49-116">Requirement</span></span> | <span data-ttu-id="36f49-117">Valor</span><span class="sxs-lookup"><span data-stu-id="36f49-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f49-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36f49-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36f49-119">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="36f49-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="36f49-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36f49-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36f49-121">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="36f49-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="36f49-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36f49-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36f49-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36f49-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f49-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="36f49-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f49-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36f49-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36f49-126">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="36f49-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="36f49-127">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="36f49-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="36f49-128">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="36f49-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="36f49-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="36f49-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




