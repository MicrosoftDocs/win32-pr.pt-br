---
description: Especifica quando um fluxo de bytes foi modificado pela última vez.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: Atributo MF_BYTESTREAM_LAST_MODIFIED_TIME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661577"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="f404d-103">\_Atributo de \_ hora da última \_ modificação \_ do MF bytes</span><span class="sxs-lookup"><span data-stu-id="f404d-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="f404d-104">Especifica quando um fluxo de bytes foi modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="f404d-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="f404d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f404d-105">Data type</span></span>

<span data-ttu-id="f404d-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="f404d-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f404d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f404d-107">Remarks</span></span>

<span data-ttu-id="f404d-108">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="f404d-108">This attribute is optional.</span></span> <span data-ttu-id="f404d-109">O valor do atributo é uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="f404d-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="f404d-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f404d-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f404d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f404d-111">Requirements</span></span>



| <span data-ttu-id="f404d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f404d-112">Requirement</span></span> | <span data-ttu-id="f404d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f404d-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f404d-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f404d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f404d-115">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="f404d-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="f404d-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f404d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f404d-117">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f404d-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="f404d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f404d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f404d-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f404d-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f404d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f404d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f404d-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f404d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f404d-122">Atributos de fluxo de bytes</span><span class="sxs-lookup"><span data-stu-id="f404d-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="f404d-123">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="f404d-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f404d-124">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="f404d-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f404d-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="f404d-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
