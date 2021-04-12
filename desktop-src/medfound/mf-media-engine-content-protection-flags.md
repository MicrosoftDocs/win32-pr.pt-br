---
description: Especifica se o mecanismo de mídia irá reproduzir conteúdo protegido.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Atributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297919"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="07433-103">\_Atributo de \_ \_ sinalizadores de proteção de conteúdo do mecanismo de \_ mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="07433-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="07433-104">Especifica se o mecanismo de mídia irá reproduzir conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="07433-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="07433-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="07433-105">Data type</span></span>

<span data-ttu-id="07433-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="07433-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="07433-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="07433-107">Remarks</span></span>

<span data-ttu-id="07433-108">O valor desse atributo é um bit a bit **ou** dos sinalizadores da enumeração de sinalizadores de [**proteção do \_ \_ mecanismo de \_ \_ mídia MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="07433-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="07433-109">Para habilitar a reprodução de conteúdo protegido, defina o sinalizador de **\_ \_ \_ habilitação de \_ \_ conteúdo protegido do MF Media Engine** .</span><span class="sxs-lookup"><span data-stu-id="07433-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="07433-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07433-110">Requirements</span></span>



| <span data-ttu-id="07433-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="07433-111">Requirement</span></span> | <span data-ttu-id="07433-112">Valor</span><span class="sxs-lookup"><span data-stu-id="07433-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="07433-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07433-113">Minimum supported client</span></span><br/> | <span data-ttu-id="07433-114">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="07433-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="07433-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07433-115">Minimum supported server</span></span><br/> | <span data-ttu-id="07433-116">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="07433-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="07433-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07433-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="07433-118"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="07433-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07433-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="07433-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07433-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07433-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="07433-121">Atributos do mecanismo de mídia</span><span class="sxs-lookup"><span data-stu-id="07433-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="07433-122">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="07433-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




