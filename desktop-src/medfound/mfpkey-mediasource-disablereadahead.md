---
description: Habilita ou desabilita o Read-Ahead em uma fonte de mídia.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Propriedade MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750147"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="5b1dd-103">\_Propriedade MFPKEY Mediate \_ DisableReadAhead</span><span class="sxs-lookup"><span data-stu-id="5b1dd-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="5b1dd-104">Habilita ou desabilita o Read-Ahead em uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="5b1dd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5b1dd-105">Data type</span></span>

<span data-ttu-id="5b1dd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5b1dd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5b1dd-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5b1dd-107">PROPVARIANT member</span></span>

<span data-ttu-id="5b1dd-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="5b1dd-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="5b1dd-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="5b1dd-109">VT\_BOOL</span></span>

<span data-ttu-id="5b1dd-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="5b1dd-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5b1dd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b1dd-111">Remarks</span></span>

<span data-ttu-id="5b1dd-112">Os aplicativos podem usar essa propriedade para configurar algumas fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="5b1dd-113">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5b1dd-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5b1dd-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5b1dd-115">Se o valor for **Variant \_ true**, a origem da mídia não será lida com antecedência no fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="5b1dd-116">Essa configuração pode otimizar o desempenho se você planeja ler uma quantidade limitada de dados da fonte de mídia, por exemplo, para obter uma imagem em miniatura de um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="5b1dd-117">Para reprodução de áudio/vídeo típica, essa propriedade deve ser definida como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="5b1dd-118">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="5b1dd-119">Nem toda fonte de mídia dá suporte a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5b1dd-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1dd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b1dd-120">Requirements</span></span>



| <span data-ttu-id="5b1dd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b1dd-121">Requirement</span></span> | <span data-ttu-id="5b1dd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5b1dd-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1dd-123">Cliente</span><span class="sxs-lookup"><span data-stu-id="5b1dd-123">Client</span></span><br/> | <span data-ttu-id="5b1dd-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5b1dd-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="5b1dd-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b1dd-125">Header</span></span><br/> | <dl> <span data-ttu-id="5b1dd-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b1dd-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1dd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b1dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1dd-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b1dd-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




