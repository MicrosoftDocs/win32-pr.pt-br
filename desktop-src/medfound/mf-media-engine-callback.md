---
description: Contém um ponteiro para a interface de retorno de chamada para o mecanismo de mídia.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: Atributo MF_MEDIA_ENGINE_CALLBACK (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782387"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="d609a-103">\_Atributo de \_ retorno de chamada do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="d609a-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="d609a-104">Contém um ponteiro para a interface de retorno de chamada para o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d609a-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d609a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d609a-105">Data type</span></span>

<span data-ttu-id="d609a-106">**IMFMediaEngineNotify \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="d609a-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="d609a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="d609a-107">Get/set</span></span>

<span data-ttu-id="d609a-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="d609a-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d609a-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="d609a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="d609a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d609a-110">Remarks</span></span>

<span data-ttu-id="d609a-111">O valor desse atributo é um ponteiro para a interface [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , implementado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d609a-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="d609a-112">Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d609a-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="d609a-113">O atributo é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d609a-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="d609a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d609a-114">Requirements</span></span>



| <span data-ttu-id="d609a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d609a-115">Requirement</span></span> | <span data-ttu-id="d609a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d609a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d609a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d609a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d609a-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d609a-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="d609a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d609a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d609a-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d609a-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d609a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d609a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d609a-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d609a-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d609a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d609a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d609a-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d609a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d609a-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d609a-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="d609a-126">**IMFMediaEngineNotify**</span><span class="sxs-lookup"><span data-stu-id="d609a-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




