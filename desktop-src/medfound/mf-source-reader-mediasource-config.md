---
description: Contém propriedades de configuração para o leitor de origem.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Atributo MF_SOURCE_READER_MEDIASOURCE_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782442"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="44229-103">\_Atributo de \_ \_ configuração de mediary do leitor de origem MF \_</span><span class="sxs-lookup"><span data-stu-id="44229-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="44229-104">Contém propriedades de configuração para o [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="44229-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="44229-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44229-105">Data type</span></span>

<span data-ttu-id="44229-106">**IPropertyStore \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="44229-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="44229-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="44229-107">Get/set</span></span>

<span data-ttu-id="44229-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="44229-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="44229-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="44229-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="44229-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="44229-110">Remarks</span></span>

<span data-ttu-id="44229-111">O valor desse atributo é um ponteiro para a interface **IPropertyStore** de um repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="44229-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="44229-112">Você pode usar esse atributo para passar Propriedades de configuração para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="44229-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="44229-113">Use este atributo com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="44229-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="44229-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="44229-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="44229-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="44229-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="44229-116">Internamente, o leitor de origem passa o ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="44229-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="44229-117">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="44229-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44229-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44229-118">Requirements</span></span>



| <span data-ttu-id="44229-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44229-119">Requirement</span></span> | <span data-ttu-id="44229-120">Valor</span><span class="sxs-lookup"><span data-stu-id="44229-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44229-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44229-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44229-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44229-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="44229-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44229-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44229-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="44229-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44229-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44229-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44229-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="44229-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44229-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="44229-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44229-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44229-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44229-129">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="44229-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="44229-130">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="44229-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




