---
description: Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Atributo MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370682"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="22691-103">\_Atributo de \_ \_ atributo somente TRANScodificação de MFT \_</span><span class="sxs-lookup"><span data-stu-id="22691-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="22691-104">Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.</span><span class="sxs-lookup"><span data-stu-id="22691-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="22691-105">Atualmente, esse atributo se aplica somente a decodificadores baseados em hardware que usam o mini-driver AVStream.</span><span class="sxs-lookup"><span data-stu-id="22691-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="22691-106">O atributo é armazenado no registro sob as informações de recursos do decodificador.</span><span class="sxs-lookup"><span data-stu-id="22691-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="22691-107">Para obter mais informações, consulte a documentação de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="22691-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="22691-108">Normalmente, os aplicativos não usam esse atributo.</span><span class="sxs-lookup"><span data-stu-id="22691-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="22691-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="22691-109">Data type</span></span>

<span data-ttu-id="22691-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="22691-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="22691-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="22691-111">Remarks</span></span>

<span data-ttu-id="22691-112">Se essa entrada de registro estiver presente e igual a 1, a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignorará o decodificador, a menos que o chamador tenha especificado o sinalizador de **enumeração de MFT de \_ \_ \_ transcodificação \_ somente** no **MFTEnumEx**.</span><span class="sxs-lookup"><span data-stu-id="22691-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="22691-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="22691-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="22691-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22691-114">Requirements</span></span>



| <span data-ttu-id="22691-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22691-115">Requirement</span></span> | <span data-ttu-id="22691-116">Valor</span><span class="sxs-lookup"><span data-stu-id="22691-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22691-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22691-117">Minimum supported client</span></span><br/> | <span data-ttu-id="22691-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="22691-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="22691-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22691-119">Minimum supported server</span></span><br/> | <span data-ttu-id="22691-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="22691-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="22691-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22691-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="22691-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="22691-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22691-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="22691-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22691-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22691-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="22691-125">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="22691-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
