---
description: A chave do registro do EUDC contém uma ou mais subchaves contendo valores que definem as fontes associadas aos caracteres definidos pelo usuário final (EUDCs) para uma determinada página de código.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766889"
---
# <a name="eudc"></a><span data-ttu-id="aa6a1-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="aa6a1-103">EUDC</span></span>

<span data-ttu-id="aa6a1-104">A chave do registro do EUDC contém uma ou mais subchaves contendo valores que definem as fontes associadas aos [caracteres definidos pelo usuário final (EUDCs)](end-user-defined-characters.md) para uma determinada página de código.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="aa6a1-105">Ele tem o seguinte local de registro:</span><span class="sxs-lookup"><span data-stu-id="aa6a1-105">It has the following registry location:</span></span>

<span data-ttu-id="aa6a1-106">HKEY \_ Current \_ user \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="aa6a1-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="aa6a1-107">O formato é:</span><span class="sxs-lookup"><span data-stu-id="aa6a1-107">The format is:</span></span>

<span data-ttu-id="aa6a1-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="aa6a1-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="aa6a1-109">onde:</span><span class="sxs-lookup"><span data-stu-id="aa6a1-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6a1-110">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="aa6a1-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="aa6a1-111">Nome predefinido usado para definir a fonte padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="aa6a1-112">Não há nenhuma fonte EUDC padrão do sistema, a menos que essa entrada seja explicitamente especificada.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="aa6a1-113">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="aa6a1-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="aa6a1-114">Nome definido pelo usuário associado a uma fonte TrueType não EUDC.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="aa6a1-115">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="aa6a1-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="aa6a1-116">Cadeia de caracteres que consiste no nome do arquivo de um arquivo de fonte EUDC separado.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="aa6a1-117">Esse arquivo identifica uma fonte a ser associada ao TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="aa6a1-118">O exemplo a seguir mostra a chave EUDC para a página de código 932.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="aa6a1-119">O exemplo a seguir define a fonte EUDC padrão do sistema como Eudc. ttf e associa as fontes EUDC separadas Mineudc. ttf e Goteudc. ttf com os nomes de fonte MS Mincho e MS Gothic, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="aa6a1-120">Quando a página de código do Windows (ACP do sistema) associada ao idioma para programas não-Unicode corresponde à subchave, o subsistema GDI procura os pares de valor de subchave para obter informações de exibição sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="aa6a1-121">Primeiro, ele procura um nome correspondente à fonte atual.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="aa6a1-122">Se não houver nenhum, ele examinará o valor SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="aa6a1-123">Se nenhum valor for definido, o GDI tratará o caractere como indefinido.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="aa6a1-124">Observe que o texto em si não precisa estar na página de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="aa6a1-125">Por exemplo, suponha que a página de código tenha o identificador 1252, a página de código padrão do Windows para inglês.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="aa6a1-126">Um aplicativo passa o ponto de código Unicode único U + E000, na área de uso privado Unicode (PUA), para [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="aa6a1-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="aa6a1-127">Nesse caso, o GDI examina os valores de registro em 1252 para obter as informações de fonte das propriedades de exibição de caractere.</span><span class="sxs-lookup"><span data-stu-id="aa6a1-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa6a1-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa6a1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa6a1-129">Entradas do registro EUDC</span><span class="sxs-lookup"><span data-stu-id="aa6a1-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="aa6a1-130">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="aa6a1-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
