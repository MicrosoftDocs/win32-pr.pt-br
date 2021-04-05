---
title: Adicionando metadados a arquivos convertidos
description: Adicionando metadados a arquivos convertidos
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, processo de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, adicionando metadados a arquivos convertidos
- adicionando metadados a arquivos convertidos
- metadados, adicionando aos arquivos convertidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641208"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="aa670-109">Adicionando metadados a arquivos convertidos</span><span class="sxs-lookup"><span data-stu-id="aa670-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="aa670-110">Os arquivos convertidos devem conter determinados metadados para garantir uma boa experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa670-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="aa670-111">No mínimo, os arquivos convertidos devem conter os atributos principais listados nas [diretrizes de uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="aa670-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="aa670-112">Para arquivos de música, defina o valor de **WM/MediaClassPrimaryID** como D1607DBC-E323-4BE2-86A1-48A42A28441E.</span><span class="sxs-lookup"><span data-stu-id="aa670-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="aa670-113">Para arquivos de caixa postal, defina o valor de **WM/MediaClassPrimaryID** como 01CD0F29-DA4E-4157-897B-6275D50C4F11, que é o GUID de classe primária para arquivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="aa670-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="aa670-114">Defina o valor de **WM/MediaClassSecondaryID** como 193c8824-4d52-4178-90bd-305240b04636.</span><span class="sxs-lookup"><span data-stu-id="aa670-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="aa670-115">Para notas de voz, defina o valor de **WM/MediaClassPrimaryID** como 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span><span class="sxs-lookup"><span data-stu-id="aa670-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="aa670-116">Defina o valor de **WM/MediaClassSecondaryID** como 3A172A13-2BD9-4831-835B-114F6A95943F.</span><span class="sxs-lookup"><span data-stu-id="aa670-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="aa670-117">Defina o valor de **WM/ContentDistributor** como o nome da chave para o serviço de música que forneceu o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aa670-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="aa670-118">Defina o valor de **WM/UniqueFileIdentifier** como a ID de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aa670-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="aa670-119">Isso permitirá que você recupere itens de conteúdo específicos em um momento futuro.</span><span class="sxs-lookup"><span data-stu-id="aa670-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="aa670-120">Defina um valor para o **WM/WMShadowFileSourceFileType**.</span><span class="sxs-lookup"><span data-stu-id="aa670-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="aa670-121">Para conteúdo protegido, use o SDK do Windows Media Format para definir o atributo **DRM \_ DRMHeader \_ ContentId** como a ID do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aa670-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="aa670-122">Para conteúdo protegido, defina um valor para **WM/WMShadowFileSourceDRMType**.</span><span class="sxs-lookup"><span data-stu-id="aa670-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa670-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa670-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa670-124">**Sobre plug-ins de conversão**</span><span class="sxs-lookup"><span data-stu-id="aa670-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="aa670-125">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="aa670-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 