---
description: Contém um ponteiro para um repositório de propriedades com propriedades de codificação.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Atributo MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662455"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="0d0df-103">\_Atributo de \_ \_ configuração do codificador do gravador de coletor MF \_</span><span class="sxs-lookup"><span data-stu-id="0d0df-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="0d0df-104">Contém um ponteiro para um repositório de propriedades com propriedades de codificação.</span><span class="sxs-lookup"><span data-stu-id="0d0df-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d0df-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0d0df-105">Data type</span></span>

<span data-ttu-id="0d0df-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="0d0df-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0df-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d0df-107">Remarks</span></span>

<span data-ttu-id="0d0df-108">O valor desse atributo é um ponteiro [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="0d0df-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="0d0df-109">Esse atributo permite que um aplicativo defina propriedades de codificação ao usar o [gravador de coletor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="0d0df-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="0d0df-110">Para definir esse atributo, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="0d0df-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="0d0df-111">Chame [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um novo repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d0df-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="0d0df-112">Defina as propriedades do codificador no repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d0df-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="0d0df-113">As propriedades disponíveis dependem do codificador.</span><span class="sxs-lookup"><span data-stu-id="0d0df-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="0d0df-114">Para obter mais informações, consulte [objetos de codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="0d0df-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="0d0df-115">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="0d0df-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="0d0df-116">Chame [**IMFAttributes:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para definir o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) no repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="0d0df-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="0d0df-117">Crie uma nova instância do gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="0d0df-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="0d0df-118">Passe o ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para a função de criação.</span><span class="sxs-lookup"><span data-stu-id="0d0df-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="0d0df-119">Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0d0df-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="0d0df-120">O gravador do coletor define as propriedades no codificador antes de definir os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d0df-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0df-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0df-121">Requirements</span></span>



| <span data-ttu-id="0d0df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d0df-122">Requirement</span></span> | <span data-ttu-id="0d0df-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0d0df-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0df-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d0df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0df-125">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d0df-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0d0df-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d0df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0df-127">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d0df-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0d0df-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d0df-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d0df-129"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d0df-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0df-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d0df-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0df-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d0df-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0d0df-132">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="0d0df-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="0d0df-133">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="0d0df-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
