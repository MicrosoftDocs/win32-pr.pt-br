---
description: O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fonte OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751218"
---
# <a name="opentype-font-format"></a><span data-ttu-id="f20af-103">Formato de fonte OpenType</span><span class="sxs-lookup"><span data-stu-id="f20af-103">OpenType Font Format</span></span>

<span data-ttu-id="f20af-104">O formato de fonte OpenType baseado em Unicode estende o formato de arquivo de fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="f20af-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="f20af-105">As fontes OpenType permitem o mapeamento entre os caracteres e os [glifos](uniscribe-glossary.md), habilitando o suporte para ligaturas, formas posicionais, alternativas e outras substituições.</span><span class="sxs-lookup"><span data-stu-id="f20af-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="f20af-106">As fontes OpenType também podem incluir informações que dão suporte a posicionamento de glifo bidimensional e anexo de glifo e podem conter contornos TrueType ou PostScript.</span><span class="sxs-lookup"><span data-stu-id="f20af-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="f20af-107">Os recursos de layout em fontes OpenType são organizados por scripts e linguagens, permitindo que uma única fonte dê suporte a vários sistemas de escrita, mesmo no mesmo script.</span><span class="sxs-lookup"><span data-stu-id="f20af-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="f20af-108">Para garantir a consistência nas operações de layout de texto e evitar sobrecarga desnecessária em arquivos de fonte ou aplicativos, muitos dos algoritmos de layout de texto e de linguagem de idioma são incluídos no Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="f20af-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="f20af-109">Isso alivia o desenvolvedor de fontes de ter que definir regras de script generalizadas dentro de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="f20af-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="f20af-110">Os aplicativos podem introduzir conhecimento ou preferências específicas sobre o layout do script.</span><span class="sxs-lookup"><span data-stu-id="f20af-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="f20af-111">Fontes de layout OpenType podem até mesmo conter regras de layout que duplicam ou substituem as aplicadas pelos serviços do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f20af-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="f20af-112">A estrutura em camadas dos serviços do sistema operacional que dá suporte ao layout de texto permite que um aplicativo escolha as informações de layout a serem usadas e selecione como aplicá-las.</span><span class="sxs-lookup"><span data-stu-id="f20af-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="f20af-113">Para obter informações adicionais, consulte a [visão geral das especificações do Microsoft Typography](https://www.microsoft.com/typography/SpecificationsOverview.mspx) ou a [especificação OpenType](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="f20af-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f20af-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f20af-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20af-115">Sobre o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="f20af-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



