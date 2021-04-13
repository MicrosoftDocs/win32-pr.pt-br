---
description: Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Atributo MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165294"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="9824f-103">\_Atributo de \_ atributo de URL de hardware de enumeração de \_ MFT \_</span><span class="sxs-lookup"><span data-stu-id="9824f-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="9824f-104">Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="9824f-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="9824f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9824f-105">Data type</span></span>

<span data-ttu-id="9824f-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9824f-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="9824f-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="9824f-107">Get/set</span></span>

<span data-ttu-id="9824f-108">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="9824f-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="9824f-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="9824f-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="9824f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9824f-110">Remarks</span></span>

<span data-ttu-id="9824f-111">Esse atributo tem suporte de MFTs baseadas em hardware.</span><span class="sxs-lookup"><span data-stu-id="9824f-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="9824f-112">O valor do atributo é o link simbólico para o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9824f-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="9824f-113">Esse atributo também é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alocados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando esses ponteiros representam MFTs baseadas em hardware.</span><span class="sxs-lookup"><span data-stu-id="9824f-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="9824f-114">O link simbólico deve ser considerado uma cadeia de caracteres opaca.</span><span class="sxs-lookup"><span data-stu-id="9824f-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="9824f-115">Para obter o nome de exibição de um dispositivo, consulte o atributo [ \_ \_ nome amigável de MFT](mft-friendly-name-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9824f-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="9824f-116">O MFTs de software não deve ter esse atributo definido.</span><span class="sxs-lookup"><span data-stu-id="9824f-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="9824f-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9824f-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9824f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9824f-118">Requirements</span></span>



| <span data-ttu-id="9824f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9824f-119">Requirement</span></span> | <span data-ttu-id="9824f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9824f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9824f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9824f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9824f-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9824f-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9824f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9824f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9824f-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9824f-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9824f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9824f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9824f-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="9824f-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9824f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9824f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9824f-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9824f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9824f-129">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="9824f-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="9824f-130">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="9824f-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




