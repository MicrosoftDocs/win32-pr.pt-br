---
title: O objeto de balão
description: O objeto de balão
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161943"
---
# <a name="the-balloon-object"></a><span data-ttu-id="197c7-103">O objeto de balão</span><span class="sxs-lookup"><span data-stu-id="197c7-103">The Balloon Object</span></span>

<span data-ttu-id="197c7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="197c7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="197c7-105">O Microsoft Agent dá suporte à legenda textual do método [**Speak**](speak-method.md) usando um balão de palavras de desenho.</span><span class="sxs-lookup"><span data-stu-id="197c7-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="197c7-106">O método [**Think**](think-method.md) permite que você exiba texto sem saída de áudio em um balão de palavras "pensados".</span><span class="sxs-lookup"><span data-stu-id="197c7-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="197c7-107">Os padrões da janela de balão inicial de um caractere são definidos e compilados no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="197c7-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="197c7-108">Uma vez em execução, as propriedades de [**fonte**](https://www.bing.com/search?q=**Font**) e [**habilitadas**](enabled-property.md) do balão podem ser substituídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="197c7-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="197c7-109">Se um usuário alterar as propriedades do balão do Word, eles afetarão todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="197c7-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="197c7-110">Os balões de [**fala**](speak-method.md) e de palavra de [**opinião**](think-method.md) usam as mesmas configurações de propriedade para tamanho.</span><span class="sxs-lookup"><span data-stu-id="197c7-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="197c7-111">Você pode acessar as propriedades do balão de palavras de um caractere por meio do objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) , que é um filho do objeto [**Character**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="197c7-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="197c7-112">O objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) dá suporte às seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="197c7-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="197c7-113">**Fundo**</span><span class="sxs-lookup"><span data-stu-id="197c7-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="197c7-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="197c7-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="197c7-115">**CharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="197c7-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="197c7-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="197c7-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="197c7-117">**FontCharSet**</span><span class="sxs-lookup"><span data-stu-id="197c7-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="197c7-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="197c7-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="197c7-119">**FontBold**</span><span class="sxs-lookup"><span data-stu-id="197c7-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="197c7-120">**FontItalic**</span><span class="sxs-lookup"><span data-stu-id="197c7-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="197c7-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="197c7-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="197c7-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="197c7-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="197c7-123">**FontUnderline**</span><span class="sxs-lookup"><span data-stu-id="197c7-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="197c7-124">**ForeColor**</span><span class="sxs-lookup"><span data-stu-id="197c7-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="197c7-125">**NumberOfLines**</span><span class="sxs-lookup"><span data-stu-id="197c7-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="197c7-126">**Estilo**</span><span class="sxs-lookup"><span data-stu-id="197c7-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="197c7-127">**Visible**</span><span class="sxs-lookup"><span data-stu-id="197c7-127">**Visible**</span></span>](visible-property-bal.md)

 

 