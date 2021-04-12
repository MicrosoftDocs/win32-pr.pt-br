---
title: Atributos globais (SDK do Windows Media Player)
description: Atributos globais
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Capas do Windows Media Player, atributos globais
- capas, atributos globais
- referência para capas, atributos globais
- atributos globais
- atributos, global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104365167"
---
# <a name="global-attributes"></a><span data-ttu-id="dda6e-108">Atributos globais</span><span class="sxs-lookup"><span data-stu-id="dda6e-108">Global Attributes</span></span>

<span data-ttu-id="dda6e-109">Atributos globais são atributos que fornecem fácil acesso a determinados elementos ou objetos do player de qualquer lugar dentro de uma capa.</span><span class="sxs-lookup"><span data-stu-id="dda6e-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="dda6e-110">O atributo global do **Player** é uma referência ao objeto do [Player](player-object.md) e é usado para acessar a funcionalidade principal do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dda6e-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="dda6e-111">O exemplo a seguir usa o **Player** para iniciar a reprodução de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="dda6e-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="dda6e-112">O atributo global **Theme** é uma referência ao elemento [Theme](theme-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dda6e-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="dda6e-113">Essa é a maneira apropriada de acessar atributos de **tema** , em vez de especificar uma ID dentro do elemento **Theme** .</span><span class="sxs-lookup"><span data-stu-id="dda6e-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="dda6e-114">O exemplo a seguir usa o **tema** para abrir uma nova exibição.</span><span class="sxs-lookup"><span data-stu-id="dda6e-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="dda6e-115">O atributo global **View** é uma referência à [exibição](view-element.md)atual.</span><span class="sxs-lookup"><span data-stu-id="dda6e-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="dda6e-116">Isso pode ser usado em vez da ID especificada nos vários elementos de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="dda6e-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="dda6e-117">O exemplo a seguir usa **View** para fechar a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="dda6e-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="dda6e-118">O atributo global de **evento** é usado para acessar os atributos de evento de ambiente a partir de manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="dda6e-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="dda6e-119">O exemplo a seguir usa o **evento** para determinar se a tecla Alt é pressionada quando um botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="dda6e-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="dda6e-120">O atributo global **playerApplication** é uma referência ao objeto [playerApplication](playerapplication-object.md) e é usado por arquivos de capa fornecidos como interfaces de usuário personalizadas para controles de Player remotos.</span><span class="sxs-lookup"><span data-stu-id="dda6e-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="dda6e-121">O controle Player só pode ser inserido no modo remoto em programas C++ que implementam a interface **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="dda6e-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="dda6e-122">O exemplo a seguir usa **playerApplication** para alternar para o modo completo do Player.</span><span class="sxs-lookup"><span data-stu-id="dda6e-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="dda6e-123">Para obter mais informações, consulte [atributos de evento de ambiente](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="dda6e-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dda6e-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dda6e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda6e-125">**Diversos**</span><span class="sxs-lookup"><span data-stu-id="dda6e-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




