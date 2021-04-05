---
description: Contém um ponteiro IMFFieldOfUseMFTUnlock, que pode ser usado para desbloquear uma Media Foundation transformação (MFT). A interface IMFFieldOfUseMFTUnlock é usada para desbloquear uma MFT que tem restrições de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Atributo MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661824"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="72620-104">\_Atributo de \_ atributo de desbloqueio de MFT FIELDOFUSE \_</span><span class="sxs-lookup"><span data-stu-id="72620-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="72620-105">Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que pode ser usado para desbloquear uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="72620-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="72620-106">A interface **IMFFieldOfUseMFTUnlock** é usada para desbloquear uma MFT que tem restrições de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="72620-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="72620-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="72620-107">Data type</span></span>

<span data-ttu-id="72620-108">**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="72620-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="72620-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="72620-109">Get/set</span></span>

<span data-ttu-id="72620-110">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="72620-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="72620-111">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="72620-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="72620-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="72620-112">Remarks</span></span>

<span data-ttu-id="72620-113">Para obter mais informações sobre esse atributo, consulte [campo de restrições de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="72620-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="72620-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="72620-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="72620-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72620-115">Requirements</span></span>



| <span data-ttu-id="72620-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72620-116">Requirement</span></span> | <span data-ttu-id="72620-117">Valor</span><span class="sxs-lookup"><span data-stu-id="72620-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72620-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72620-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72620-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="72620-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="72620-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72620-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72620-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="72620-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="72620-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72620-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72620-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="72620-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72620-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="72620-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72620-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72620-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="72620-126">Campo de restrições de uso</span><span class="sxs-lookup"><span data-stu-id="72620-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="72620-127">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="72620-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




