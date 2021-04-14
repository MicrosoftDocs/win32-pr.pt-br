---
description: Contém um ponteiro para a interface IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: Atributo MF_MEDIA_ENGINE_EXTENSION (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104370822"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="3ba5a-103">\_Atributo de \_ extensão do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="3ba5a-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="3ba5a-104">Contém um ponteiro para a interface [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="3ba5a-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ba5a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3ba5a-105">Data type</span></span>

<span data-ttu-id="3ba5a-106">**IMFMediaEngineExtension \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="3ba5a-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="3ba5a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="3ba5a-107">Get/set</span></span>

<span data-ttu-id="3ba5a-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="3ba5a-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="3ba5a-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="3ba5a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba5a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba5a-110">Remarks</span></span>

<span data-ttu-id="3ba5a-111">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3ba5a-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="3ba5a-112">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="3ba5a-112">This attribute is optional.</span></span> <span data-ttu-id="3ba5a-113">Use-o para fornecer um objeto que implementa a interface [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="3ba5a-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="3ba5a-114">Essa interface permite que o aplicativo carregue recursos de mídia personalizados.</span><span class="sxs-lookup"><span data-stu-id="3ba5a-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba5a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba5a-115">Requirements</span></span>



| <span data-ttu-id="3ba5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba5a-116">Requirement</span></span> | <span data-ttu-id="3ba5a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba5a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba5a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba5a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba5a-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ba5a-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="3ba5a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba5a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba5a-121">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ba5a-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="3ba5a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ba5a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba5a-123"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba5a-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba5a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba5a-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ba5a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




