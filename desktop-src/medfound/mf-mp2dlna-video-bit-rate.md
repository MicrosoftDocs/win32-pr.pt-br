---
description: Especifica a taxa máxima de bits de vídeo para o coletor de mídia DLNA (rede de vida digital).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Atributo MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165025"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="bdc12-103">\_Atributo de \_ taxa de bits de vídeo MF MP2DLNA \_ \_</span><span class="sxs-lookup"><span data-stu-id="bdc12-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="bdc12-104">Especifica a taxa máxima de bits de vídeo para o coletor de mídia DLNA (rede de vida digital).</span><span class="sxs-lookup"><span data-stu-id="bdc12-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="bdc12-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bdc12-105">Data type</span></span>

<span data-ttu-id="bdc12-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bdc12-106">**UINT32**</span></span>

<span data-ttu-id="bdc12-107">O valor é a taxa de bits máxima de destino para o fluxo de vídeo codificado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bdc12-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="bdc12-108">O valor máximo é 9,8 milhões (9,8 Mbps), que também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="bdc12-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="bdc12-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="bdc12-109">Get/set</span></span>

<span data-ttu-id="bdc12-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="bdc12-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="bdc12-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="bdc12-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc12-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdc12-112">Remarks</span></span>

<span data-ttu-id="bdc12-113">Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="bdc12-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="bdc12-114">Defina o atributo antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="bdc12-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc12-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc12-115">Requirements</span></span>



| <span data-ttu-id="bdc12-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc12-116">Requirement</span></span> | <span data-ttu-id="bdc12-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc12-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc12-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc12-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc12-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bdc12-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bdc12-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdc12-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc12-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bdc12-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bdc12-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdc12-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc12-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc12-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc12-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdc12-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc12-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdc12-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




