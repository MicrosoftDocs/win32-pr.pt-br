---
title: Interface IWMPClosedCaption (VB e C) (WMP. h)
description: Fornece uma maneira de incluir legendas com um arquivo de mídia digital. O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- IWMPClosedCaption (VB e C) interface do Windows Media Player
- IWMPClosedCaption (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761441"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="08f09-106">Interface IWMPClosedCaption (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="08f09-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="08f09-107">Fornece uma maneira de incluir legendas com um arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="08f09-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="08f09-108">O texto da legenda está em um arquivo de intercâmbio de mídia acessível (SAMI) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="08f09-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="08f09-109">Membros</span><span class="sxs-lookup"><span data-stu-id="08f09-109">Members</span></span>

<span data-ttu-id="08f09-110">A interface **IWMPClosedCaption (VB e C#)** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="08f09-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="08f09-111">A interface **IWMPClosedCaption** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="08f09-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="08f09-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="08f09-112">Property</span></span>                                                                             | <span data-ttu-id="08f09-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="08f09-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f09-114">captioningId</span><span class="sxs-lookup"><span data-stu-id="08f09-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="08f09-115">Obtém ou define o nome do elemento HTML que exibe a legenda.</span><span class="sxs-lookup"><span data-stu-id="08f09-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="08f09-116">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="08f09-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="08f09-117">Obtém ou define o nome do arquivo que contém as informações necessárias para a legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="08f09-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="08f09-118">SAMILang</span><span class="sxs-lookup"><span data-stu-id="08f09-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="08f09-119">Obtém ou define o idioma exibido para Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="08f09-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="08f09-120">SAMIstyle</span><span class="sxs-lookup"><span data-stu-id="08f09-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="08f09-121">Obtém ou define o estilo de legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="08f09-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="08f09-122">Obtenha uma interface **IWMPClosedCaption** usando a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="08f09-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="08f09-123">Objeto</span><span class="sxs-lookup"><span data-stu-id="08f09-123">Object</span></span>                                                            | <span data-ttu-id="08f09-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="08f09-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="08f09-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="08f09-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="08f09-126">closedCaption</span><span class="sxs-lookup"><span data-stu-id="08f09-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="08f09-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f09-127">Requirements</span></span>



| <span data-ttu-id="08f09-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f09-128">Requirement</span></span> | <span data-ttu-id="08f09-129">Valor</span><span class="sxs-lookup"><span data-stu-id="08f09-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08f09-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08f09-130">Header</span></span><br/> | <dl> <span data-ttu-id="08f09-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f09-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08f09-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="08f09-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f09-133">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="08f09-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="08f09-134">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="08f09-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="08f09-135">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="08f09-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





