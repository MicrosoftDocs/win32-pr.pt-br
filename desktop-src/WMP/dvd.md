---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrando DVDs
- Modelo de objeto do Windows Media Player, DVDs
- modelo de objeto, DVDs
- Controle ActiveX do Windows Media Player, DVDs
- Controle ActiveX, DVDs
- Controle ActiveX móvel do Windows Media Player, DVDs
- Windows Media Player Mobile, migrando DVDs
- Guia de migração, DVDs
- Migração de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636277"
---
# <a name="dvd"></a><span data-ttu-id="e5cd9-112">DVD</span><span class="sxs-lookup"><span data-stu-id="e5cd9-112">DVD</span></span>

<span data-ttu-id="e5cd9-113">O controle ActiveX do Windows Media Player 6,4 contém um objeto de **DVD** que expõe uma variedade de métodos e propriedades e um evento, para lidar especificamente com conteúdo de DVD.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="e5cd9-114">Por exemplo, para determinar o número de títulos de DVD disponíveis, use o **Player6**. Propriedade **titlesAvailable** :</span><span class="sxs-lookup"><span data-stu-id="e5cd9-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="e5cd9-115">O modelo de objeto do Windows Media Player 7 ou posterior implementa uma abordagem mais integrada ao DVD.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="e5cd9-116">Propriedades, métodos e eventos específicos de DVD são implementados somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="e5cd9-117">Caso contrário, a funcionalidade de modelo de objeto existente funciona com mídia de DVD como você pode esperar.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="e5cd9-118">Por exemplo, para determinar o número de títulos de DVD disponíveis ao usar o Windows Media Player 7 ou posterior, você recupera um objeto de **playlist** do objeto de **cdrom** :</span><span class="sxs-lookup"><span data-stu-id="e5cd9-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="e5cd9-119">O exemplo anterior recupera um objeto de **playlist** com uma primeira entrada que representa a mídia de DVD na primeira unidade.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="e5cd9-120">Entradas adicionais representam títulos de DVD individuais.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="e5cd9-121">Portanto, o número de títulos disponíveis pode ser calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e5cd9-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="e5cd9-122">Aqui estão as principais diferenças a serem consideradas ao migrar da versão 6,4:</span><span class="sxs-lookup"><span data-stu-id="e5cd9-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="e5cd9-123">A reprodução de DVD tem suporte apenas ao usar o Windows Media Player para Windows XP ou posterior e o sistema operacional Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="e5cd9-124">As unidades de DVD-ROM são enumeradas exatamente como unidades de CD-ROM usando o objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="e5cd9-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="e5cd9-125">Unidades de DVD-ROM individuais são gerenciadas usando o objeto **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="e5cd9-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="e5cd9-126">O objeto **DVD** estende o modelo de objeto com métodos e uma propriedade especificamente para trabalhar com o DVD.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="e5cd9-127">Há dois novos eventos, **OpenPlaylistSwitch** e **DomainChange**, especificamente para trabalhar com DVD.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="e5cd9-128">O conteúdo do DVD é organizado usando objetos de **lista de reprodução** e objetos de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e5cd9-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="e5cd9-129">As linguagens de DVD são gerenciadas usando a funcionalidade de linguagem disponível no objeto de **controles** (Windows Media Player 9 Series ou posterior).</span><span class="sxs-lookup"><span data-stu-id="e5cd9-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="e5cd9-130">Os controles de transporte e as informações de posição para DVD funcionam da mesma forma que para outros tipos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="e5cd9-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5cd9-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5cd9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5cd9-132">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="e5cd9-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="e5cd9-133">**Usando o controle do Windows Media Player com Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="e5cd9-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




