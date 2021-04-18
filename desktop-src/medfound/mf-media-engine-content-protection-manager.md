---
description: Permite que o mecanismo de mídia Reproduza conteúdo protegido.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Atributo MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784522"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="2366c-103">\_Atributo do \_ \_ \_ \_ Gerenciador de mídia MF</span><span class="sxs-lookup"><span data-stu-id="2366c-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="2366c-104">Permite que o mecanismo de mídia Reproduza conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="2366c-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="2366c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2366c-105">Data type</span></span>

<span data-ttu-id="2366c-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="2366c-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="2366c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2366c-107">Remarks</span></span>

<span data-ttu-id="2366c-108">O valor desse atributo é um ponteiro para a interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="2366c-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="2366c-109">O chamador deve implementar a interface.</span><span class="sxs-lookup"><span data-stu-id="2366c-109">The caller must implement the interface.</span></span>

<span data-ttu-id="2366c-110">Esse atributo pode ser um dos atributos passados para [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="2366c-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="2366c-111">Será necessário se o conteúdo protegido for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="2366c-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="2366c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2366c-112">Requirements</span></span>



| <span data-ttu-id="2366c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2366c-113">Requirement</span></span> | <span data-ttu-id="2366c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2366c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2366c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2366c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2366c-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2366c-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="2366c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2366c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2366c-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2366c-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="2366c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2366c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2366c-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="2366c-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2366c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2366c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2366c-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2366c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2366c-123">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="2366c-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




