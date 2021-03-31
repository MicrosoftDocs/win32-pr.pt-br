---
title: Fornecendo uma interface do usuário
description: Fornecendo uma interface do usuário
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades
- plug-ins, páginas de propriedades
- plug-ins de processamento de sinal digital, páginas de propriedades
- Plug-ins do DSP, páginas de propriedades
- plug-ins de processamento de sinal digital, interface do usuário
- Plug-ins do DSP, interface do usuário
- páginas de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160221"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="d1e8a-110">Fornecendo uma interface do usuário</span><span class="sxs-lookup"><span data-stu-id="d1e8a-110">Providing a User Interface</span></span>

<span data-ttu-id="d1e8a-111">Plug-ins do DSP podem fornecer uma página de propriedades para criar uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="d1e8a-112">Para fazer isso, o plug-in deve incluir um objeto de página de propriedades que fornece uma implementação de uma interface **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="d1e8a-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="d1e8a-113">O objeto de plug-in DSP deve implementar **ISpecifyPropertyPages:: GetPages**, que permite que o Windows Media Player Localize e identifique a página de propriedades correta para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="d1e8a-114">**Exibindo um gráfico de status**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="d1e8a-115">Plug-ins DSP podem exibir um elemento gráfico pequeno ou uma série de gráficos, na área status do Windows Media Player, para notificar o usuário de que um plug-in está ativo.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="d1e8a-116">Para dar suporte a esse recurso, o plug-in deve implementar a interface **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="d1e8a-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="d1e8a-117">O Windows Media Player chama **IPropertyBag:: Read**, fornecendo um ponteiro para o nome da propriedade solicitada "iconstreams", que diferencia maiúsculas de minúsculas e um ponteiro para uma estrutura **variante** que recebe os dados para o gráfico.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="d1e8a-118">O plug-in cria um objeto **IStream** (ou um SafeArray de objetos **IStream** se houver vários gráficos) e, em seguida, carrega os dados gráficos, incluindo informações de cabeçalho, para o fluxo e, em seguida, retorna um ponteiro para o objeto **IStream** usando o membro **punkVal** da estrutura **Variant** .</span><span class="sxs-lookup"><span data-stu-id="d1e8a-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="d1e8a-119">Se o plug-in fornecer apenas um gráfico, ele especificará o membro **VT** da estrutura **Variant** como VT \_ desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="d1e8a-120">Se o plug-in fornecer vários objetos de **IStream** gráfico usando um SafeArray, ele especificará o membro **VT** da estrutura **Variant** como a \_ matriz VT.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="d1e8a-121">Os gráficos podem ser armazenados em uma variedade de formatos de arquivo, incluindo:</span><span class="sxs-lookup"><span data-stu-id="d1e8a-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="d1e8a-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-122">**BMP**</span></span>

<span data-ttu-id="d1e8a-123">As imagens de bitmap do Microsoft Windows são descompactadas.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="d1e8a-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-124">**JPEG**</span></span>

<span data-ttu-id="d1e8a-125">Formato de imagem compactado normalmente usado para páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="d1e8a-126">Os arquivos de formato JPEG geralmente têm extensões de nome de arquivo. jpg.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="d1e8a-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-127">**GIF**</span></span>

<span data-ttu-id="d1e8a-128">Formato de imagem compactado normalmente usado para páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="d1e8a-129">**PNG**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-129">**PNG**</span></span>

<span data-ttu-id="d1e8a-130">Formato de imagem compactado normalmente usado para páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="d1e8a-131">As dimensões máximas para gráficos de plug-in DSP têm 38 pixels de largura e 14 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="d1e8a-132">O fluxo de bytes de **IStream** que contém o gráfico de status deve incluir informações de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="d1e8a-133">Sem informações de cabeçalho, o Windows Media Player não pode identificar corretamente o tipo de elemento gráfico e, portanto, não carregará a imagem.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1e8a-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1e8a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e8a-135">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="d1e8a-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




