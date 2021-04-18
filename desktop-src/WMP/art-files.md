---
title: Arquivos de arte
description: Arquivos de arte
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Capas do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781465"
---
# <a name="art-files"></a><span data-ttu-id="87838-107">Arquivos de arte</span><span class="sxs-lookup"><span data-stu-id="87838-107">Art Files</span></span>

<span data-ttu-id="87838-108">Você deve criar um ou mais arquivos de arte para sua capa.</span><span class="sxs-lookup"><span data-stu-id="87838-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="87838-109">Sem arte, o usuário não terá nada a ver.</span><span class="sxs-lookup"><span data-stu-id="87838-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="87838-110">Você poderia criar uma capa invisível, mas ninguém verá!</span><span class="sxs-lookup"><span data-stu-id="87838-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="87838-111">E mesmo assim, você ainda precisaria criar arquivos Art para manter suas imagens invisíveis, pois o arquivo de definição de capa requer arquivos Art para elementos específicos.</span><span class="sxs-lookup"><span data-stu-id="87838-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="87838-112">Há três usos para arte em capas: imagens primárias, imagens de mapeamento e imagens alternativas.</span><span class="sxs-lookup"><span data-stu-id="87838-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="87838-113">Imagens primárias</span><span class="sxs-lookup"><span data-stu-id="87838-113">Primary Images</span></span>

<span data-ttu-id="87838-114">Você deve criar uma imagem primária para sua capa.</span><span class="sxs-lookup"><span data-stu-id="87838-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="87838-115">Isso é o que os usuários verão quando instalarem sua capa.</span><span class="sxs-lookup"><span data-stu-id="87838-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="87838-116">A imagem primária é composta de uma ou mais imagens que são criadas por controles de capa específicos.</span><span class="sxs-lookup"><span data-stu-id="87838-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="87838-117">Se você tiver mais de um controle, deverá especificar a ordem z, que define quais controles são exibidos na frente de outros controles.</span><span class="sxs-lookup"><span data-stu-id="87838-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="87838-118">Cada elemento de **exibição** terá uma imagem de plano de fundo à qual você pode adicionar outras imagens de elemento, permitindo que você crie uma imagem composta primária.</span><span class="sxs-lookup"><span data-stu-id="87838-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="87838-119">Você também pode ter imagens secundárias, como uma bandeja deslizante, que não são exibidas quando sua aparência é exibida pela primeira vez, mas que aparecem quando o usuário executa alguma ação.</span><span class="sxs-lookup"><span data-stu-id="87838-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="87838-120">Eles seguem as mesmas regras que as imagens primárias, pois elas são criadas com um conjunto de controles.</span><span class="sxs-lookup"><span data-stu-id="87838-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="87838-121">Mapeando imagens</span><span class="sxs-lookup"><span data-stu-id="87838-121">Mapping Images</span></span>

<span data-ttu-id="87838-122">Um dos recursos mais poderosos das capas do Windows Media Player é que você pode usar o mapeamento de imagem para disparar eventos para sua capa.</span><span class="sxs-lookup"><span data-stu-id="87838-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="87838-123">Mapas de imagem são arquivos que contêm imagens especiais.</span><span class="sxs-lookup"><span data-stu-id="87838-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="87838-124">As imagens em um arquivo de mapa de imagem, no entanto, não devem ser exibidas pelo usuário, mas são usadas pelo Windows Media Player para executar uma ação quando o usuário clica em sua capa.</span><span class="sxs-lookup"><span data-stu-id="87838-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="87838-125">Controles diferentes precisam de diferentes tipos de mapas de imagem.</span><span class="sxs-lookup"><span data-stu-id="87838-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="87838-126">Por exemplo, se você colorir parte de um mapa de imagem de um valor vermelho específico e o usuário clicar na área correspondente da imagem primária, um botão acionará um evento.</span><span class="sxs-lookup"><span data-stu-id="87838-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="87838-127">A cor é usada para definir quais eventos são disparados clicando em uma área específica da capa.</span><span class="sxs-lookup"><span data-stu-id="87838-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="87838-128">Imagens alternativas</span><span class="sxs-lookup"><span data-stu-id="87838-128">Alternate Images</span></span>

<span data-ttu-id="87838-129">Você também pode configurar imagens alternativas para exibir quando um usuário faz algo.</span><span class="sxs-lookup"><span data-stu-id="87838-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="87838-130">Por exemplo, você pode criar uma imagem alternativa de um botão que será exibido somente quando o mouse passar sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="87838-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="87838-131">Essa é uma boa maneira de permitir que os usuários saibam o que eles podem fazer e também permite uma interface do usuário altamente detectável.</span><span class="sxs-lookup"><span data-stu-id="87838-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="87838-132">Usando dicas de ferramentas e focalizar imagens com cuidado, você pode criar interfaces de usuário incomuns que ainda dão ao usuário comentários sobre quais opções estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87838-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="87838-133">As seções a seguir fornecem mais informações sobre arquivos de arte:</span><span class="sxs-lookup"><span data-stu-id="87838-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="87838-134">Imagens primárias</span><span class="sxs-lookup"><span data-stu-id="87838-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="87838-135">Mapeando imagens</span><span class="sxs-lookup"><span data-stu-id="87838-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="87838-136">Imagens alternativas</span><span class="sxs-lookup"><span data-stu-id="87838-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="87838-137">Formatos de arquivo artístico</span><span class="sxs-lookup"><span data-stu-id="87838-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="87838-138">Exemplo de arte simples</span><span class="sxs-lookup"><span data-stu-id="87838-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="87838-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87838-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87838-140">**Arquivos de capa**</span><span class="sxs-lookup"><span data-stu-id="87838-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




