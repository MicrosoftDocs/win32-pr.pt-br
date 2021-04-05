---
description: Especifica o &\# 0034; Bucket de vazamento&\# 0034; parâmetros para um fluxo em um coletor de mídia ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Propriedade MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827307"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="94974-103">\_ \_ Propriedade LEAKYBUCKET MFPKEY ASFSTREAMSINK corrigida \_</span><span class="sxs-lookup"><span data-stu-id="94974-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="94974-104">Especifica os parâmetros de "Bucket de vazamentos" (consulte comentários) para um fluxo em um coletor de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="94974-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="94974-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="94974-105">Data type</span></span>

<span data-ttu-id="94974-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="94974-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="94974-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="94974-107">PROPVARIANT member</span></span>

<span data-ttu-id="94974-108">Matriz de valores **DWORD** (**Caul**)</span><span class="sxs-lookup"><span data-stu-id="94974-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="94974-109">\_UI4 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="94974-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="94974-110">**caul**</span><span class="sxs-lookup"><span data-stu-id="94974-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="94974-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="94974-111">Remarks</span></span>

<span data-ttu-id="94974-112">Um aplicativo pode definir essa propriedade em um fluxo do coletor de mídia ASF depois que o tipo de mídia para o fluxo é negociado.</span><span class="sxs-lookup"><span data-stu-id="94974-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="94974-113">Use essa propriedade para especificar a janela de buffer real que o Windows Media Codec usará.</span><span class="sxs-lookup"><span data-stu-id="94974-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="94974-114">Você pode obter essas informações do codec usando a interface **IWMCodecLeakyBucket** , que está documentada no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="94974-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="94974-115">O valor dessa propriedade é uma matriz de três valores **DWORD** na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="94974-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="94974-116">Taxa de bits, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="94974-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="94974-117">Tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94974-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="94974-118">Total do buffer inicial, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94974-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="94974-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94974-119">Requirements</span></span>



| <span data-ttu-id="94974-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="94974-120">Requirement</span></span> | <span data-ttu-id="94974-121">Valor</span><span class="sxs-lookup"><span data-stu-id="94974-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94974-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94974-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94974-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94974-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="94974-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94974-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94974-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94974-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="94974-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94974-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94974-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94974-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94974-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="94974-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94974-129">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="94974-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="94974-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94974-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




