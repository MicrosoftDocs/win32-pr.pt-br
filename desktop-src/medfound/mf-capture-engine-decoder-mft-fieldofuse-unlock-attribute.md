---
description: Permite que o mecanismo de captura use um decodificador com restrições de campo de uso.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Atributo MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787700"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="127c2-103">\_FIELDOFUSE de \_ \_ atributo do \_ \_ \_ desbloqueio \_ do mecanismo de captura do MF MFT</span><span class="sxs-lookup"><span data-stu-id="127c2-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="127c2-104">Permite que o mecanismo de captura use um decodificador com restrições de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="127c2-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="127c2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="127c2-105">Data type</span></span>

<span data-ttu-id="127c2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="127c2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="127c2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="127c2-107">Remarks</span></span>

<span data-ttu-id="127c2-108">O valor desse atributo é um ponteiro para a interface [_ *IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="127c2-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="127c2-109">Espera-se que a implementação dessa interface do chamador execute um handshake com o decodificador, conforme descrito em [campo de restrições de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="127c2-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="127c2-110">Microsoft Media Foundation não define o handshake — normalmente, ele envolveria algum tipo de troca de criptografia.</span><span class="sxs-lookup"><span data-stu-id="127c2-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="127c2-111">Internamente, o mecanismo de captura define o ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) no decodificador definindo o atributo [de \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) do decodificador.</span><span class="sxs-lookup"><span data-stu-id="127c2-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="127c2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="127c2-112">Requirements</span></span>



| <span data-ttu-id="127c2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="127c2-113">Requirement</span></span> | <span data-ttu-id="127c2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="127c2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="127c2-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="127c2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="127c2-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="127c2-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="127c2-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="127c2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="127c2-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="127c2-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="127c2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="127c2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="127c2-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="127c2-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127c2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="127c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127c2-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="127c2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="127c2-123">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="127c2-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="127c2-124">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="127c2-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




