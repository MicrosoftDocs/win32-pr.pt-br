---
title: Objeto ClosedCaption
description: O objeto ClosedCaption fornece uma maneira de incluir legendas com um clipe de mídia. O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objeto ClosedCaption Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006763"
---
# <a name="closedcaption-object"></a><span data-ttu-id="f53ca-105">Objeto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="f53ca-105">ClosedCaption Object</span></span>

<span data-ttu-id="f53ca-106">O objeto **ClosedCaption** fornece uma maneira de incluir legendas com um clipe de mídia.</span><span class="sxs-lookup"><span data-stu-id="f53ca-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="f53ca-107">O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="f53ca-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="f53ca-108">O objeto **ClosedCaption** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="f53ca-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="f53ca-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f53ca-109">Property</span></span>                                           | <span data-ttu-id="f53ca-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f53ca-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f53ca-111">captioningID</span><span class="sxs-lookup"><span data-stu-id="f53ca-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="f53ca-112">Especifica ou recupera o nome do quadro ou controle que exibe a legenda.</span><span class="sxs-lookup"><span data-stu-id="f53ca-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="f53ca-113">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="f53ca-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="f53ca-114">Especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="f53ca-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="f53ca-115">SAMILang</span><span class="sxs-lookup"><span data-stu-id="f53ca-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="f53ca-116">Especifica ou recupera o idioma exibido para legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="f53ca-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="f53ca-117">SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="f53ca-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="f53ca-118">Recupera o número de idiomas com suporte pelo arquivo SAMI atual.</span><span class="sxs-lookup"><span data-stu-id="f53ca-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="f53ca-119">SAMIstyle</span><span class="sxs-lookup"><span data-stu-id="f53ca-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="f53ca-120">Especifica ou recupera o estilo de legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="f53ca-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="f53ca-121">SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="f53ca-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="f53ca-122">Recupera o número de estilos com suporte pelo arquivo SAMI atual.</span><span class="sxs-lookup"><span data-stu-id="f53ca-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="f53ca-123">O objeto **ClosedCaption** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f53ca-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="f53ca-124">Método</span><span class="sxs-lookup"><span data-stu-id="f53ca-124">Method</span></span>                                                 | <span data-ttu-id="f53ca-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="f53ca-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f53ca-126">getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="f53ca-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="f53ca-127">Recupera o identificador de localidade (LCID) de um idioma com suporte do arquivo SAMI atual.</span><span class="sxs-lookup"><span data-stu-id="f53ca-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="f53ca-128">getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="f53ca-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="f53ca-129">Recupera o nome de um idioma com suporte no arquivo SAMI atual.</span><span class="sxs-lookup"><span data-stu-id="f53ca-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="f53ca-130">getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="f53ca-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="f53ca-131">Recupera o nome de um estilo suportado pelo arquivo SAMI atual.</span><span class="sxs-lookup"><span data-stu-id="f53ca-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="f53ca-132">O objeto **ClosedCaption** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="f53ca-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="f53ca-133">Objeto</span><span class="sxs-lookup"><span data-stu-id="f53ca-133">Object</span></span>                      | <span data-ttu-id="f53ca-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f53ca-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="f53ca-135">Jogador</span><span class="sxs-lookup"><span data-stu-id="f53ca-135">Player</span></span>](player-object.md) | [<span data-ttu-id="f53ca-136">closedCaption</span><span class="sxs-lookup"><span data-stu-id="f53ca-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="f53ca-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f53ca-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53ca-138">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="f53ca-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f53ca-139">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="f53ca-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




