---
description: Contém o nome de exibição para uma transformação de Media Foundation baseada em hardware (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Atributo MFT_FRIENDLY_NAME_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752351"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="5dcbc-103">\_Atributo de \_ atributo de nome amigável de MFT \_</span><span class="sxs-lookup"><span data-stu-id="5dcbc-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="5dcbc-104">Contém o nome de exibição para uma transformação de Media Foundation baseada em hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="5dcbc-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="5dcbc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5dcbc-105">Data type</span></span>

<span data-ttu-id="5dcbc-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5dcbc-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="5dcbc-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5dcbc-107">Get/set</span></span>

<span data-ttu-id="5dcbc-108">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="5dcbc-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="5dcbc-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="5dcbc-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="5dcbc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dcbc-110">Remarks</span></span>

<span data-ttu-id="5dcbc-111">Esse atributo tem suporte de MFTs baseadas em hardware.</span><span class="sxs-lookup"><span data-stu-id="5dcbc-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="5dcbc-112">Ele também é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alocados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando esses ponteiros representam MFTs baseadas em hardware.</span><span class="sxs-lookup"><span data-stu-id="5dcbc-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="5dcbc-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5dcbc-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dcbc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dcbc-114">Requirements</span></span>



| <span data-ttu-id="5dcbc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dcbc-115">Requirement</span></span> | <span data-ttu-id="5dcbc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5dcbc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dcbc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dcbc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5dcbc-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5dcbc-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5dcbc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dcbc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5dcbc-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="5dcbc-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5dcbc-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dcbc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dcbc-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dcbc-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dcbc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dcbc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dcbc-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5dcbc-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5dcbc-125">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="5dcbc-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




