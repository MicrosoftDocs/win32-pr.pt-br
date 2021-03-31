---
description: Especifica a taxa máxima de bits de áudio para o coletor de mídia DLNA (rede de vida digital).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Atributo MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921271"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="71102-103">\_Atributo de \_ taxa de bits de áudio MF MP2DLNA \_ \_</span><span class="sxs-lookup"><span data-stu-id="71102-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="71102-104">Especifica a taxa máxima de bits de áudio para o coletor de mídia DLNA (rede de vida digital).</span><span class="sxs-lookup"><span data-stu-id="71102-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="71102-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="71102-105">Data type</span></span>

<span data-ttu-id="71102-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="71102-106">**UINT32**</span></span>

<span data-ttu-id="71102-107">O valor é a taxa de bits máxima de destino para o fluxo de áudio codificado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="71102-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="71102-108">O valor deve ser uma das taxas de bits permitidas para áudio MPEG-2 Layer 2 para DLNA.</span><span class="sxs-lookup"><span data-stu-id="71102-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="71102-109">O valor padrão é 192000 (192 kbps).</span><span class="sxs-lookup"><span data-stu-id="71102-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="71102-110">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="71102-110">Get/set</span></span>

<span data-ttu-id="71102-111">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="71102-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="71102-112">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="71102-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="71102-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="71102-113">Remarks</span></span>

<span data-ttu-id="71102-114">Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="71102-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="71102-115">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="71102-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="71102-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71102-116">Requirements</span></span>



| <span data-ttu-id="71102-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71102-117">Requirement</span></span> | <span data-ttu-id="71102-118">Valor</span><span class="sxs-lookup"><span data-stu-id="71102-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71102-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71102-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71102-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71102-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="71102-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71102-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71102-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="71102-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="71102-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71102-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71102-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="71102-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71102-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="71102-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71102-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71102-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




