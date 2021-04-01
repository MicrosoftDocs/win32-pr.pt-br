---
description: Esse atributo especifica proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Atributo MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921222"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="93cd2-103">\_Atributo MFPROTECTION CONSTRICTVIDEO \_ NOOPM</span><span class="sxs-lookup"><span data-stu-id="93cd2-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="93cd2-104">Esse atributo especifica proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="93cd2-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="93cd2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="93cd2-105">Data type</span></span>

<span data-ttu-id="93cd2-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="93cd2-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="93cd2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="93cd2-107">Remarks</span></span>

<span data-ttu-id="93cd2-108">Essa é uma proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída (consulte [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="93cd2-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="93cd2-109">Nesse caso, o OTA pode oferecer essa proteção cujo efeito é o mesmo que a proteção [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="93cd2-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="93cd2-110">Isso é definido para evitar confusão com chamadas anteriores a [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interações em que a presença da proteção do MFPROTECTION \_ CONSTRICTVIDEO foi usada para ajudar a identificar o pseudodispositivo do Gerenciador de janelas da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93cd2-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="93cd2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93cd2-111">Requirements</span></span>



| <span data-ttu-id="93cd2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="93cd2-112">Requirement</span></span> | <span data-ttu-id="93cd2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="93cd2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93cd2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93cd2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="93cd2-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93cd2-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="93cd2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93cd2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="93cd2-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="93cd2-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="93cd2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93cd2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="93cd2-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="93cd2-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93cd2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="93cd2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93cd2-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93cd2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




