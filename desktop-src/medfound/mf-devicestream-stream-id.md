---
description: Especifica o identificador de streaming de kernel (KS) para um fluxo em um dispositivo de captura de vídeo.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: Atributo MF_DEVICESTREAM_STREAM_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010721"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="53543-103">\_Atributo de \_ ID de fluxo MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="53543-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="53543-104">Especifica o identificador de streaming de kernel (KS) para um fluxo em um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="53543-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="53543-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="53543-105">Data type</span></span>

<span data-ttu-id="53543-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53543-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="53543-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="53543-107">Remarks</span></span>

<span data-ttu-id="53543-108">Para obter esse atributo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53543-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="53543-109">Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="53543-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="53543-110">Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="53543-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="53543-111">Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="53543-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="53543-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53543-112">Requirements</span></span>



| <span data-ttu-id="53543-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="53543-113">Requirement</span></span> | <span data-ttu-id="53543-114">Valor</span><span class="sxs-lookup"><span data-stu-id="53543-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53543-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53543-115">Minimum supported client</span></span><br/> | <span data-ttu-id="53543-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="53543-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53543-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53543-117">Minimum supported server</span></span><br/> | <span data-ttu-id="53543-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="53543-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="53543-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53543-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="53543-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53543-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53543-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="53543-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53543-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53543-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




