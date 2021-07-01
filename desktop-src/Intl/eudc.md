---
description: A chave do Registro EUDC contém uma ou mais sub-chaves que contêm valores que definem as fontes associadas aos EUDCs (caracteres definidos pelo usuário final) para uma determinada página de código.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: Eudc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120701"
---
# <a name="eudc"></a><span data-ttu-id="fd515-103">Eudc</span><span class="sxs-lookup"><span data-stu-id="fd515-103">EUDC</span></span>

<span data-ttu-id="fd515-104">A chave do Registro EUDC contém uma ou mais sub-chaves que contêm valores que definem as fontes associadas aos [EUDCs (caracteres](end-user-defined-characters.md) definidos pelo usuário final) para uma determinada página de código.</span><span class="sxs-lookup"><span data-stu-id="fd515-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="fd515-105">Ele tem o seguinte local do Registro:</span><span class="sxs-lookup"><span data-stu-id="fd515-105">It has the following registry location:</span></span>

<span data-ttu-id="fd515-106">\_ \_ EUDC DO USUÁRIO ATUAL \\ DO HKEY</span><span class="sxs-lookup"><span data-stu-id="fd515-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="fd515-107">O formato é:</span><span class="sxs-lookup"><span data-stu-id="fd515-107">The format is:</span></span>

<span data-ttu-id="fd515-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="fd515-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="fd515-109">em que:</span><span class="sxs-lookup"><span data-stu-id="fd515-109">where:</span></span>



| <span data-ttu-id="fd515-110">Valor</span><span class="sxs-lookup"><span data-stu-id="fd515-110">Value</span></span>                         | <span data-ttu-id="fd515-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd515-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd515-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="fd515-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="fd515-113">Nome predefinido usado para definir a fonte padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="fd515-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="fd515-114">Não há nenhuma fonte EUDC padrão do sistema, a menos que essa entrada seja especificada explicitamente.</span><span class="sxs-lookup"><span data-stu-id="fd515-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="fd515-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="fd515-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="fd515-116">Nome definido pelo usuário associado a uma fonte TrueType não EUDC.</span><span class="sxs-lookup"><span data-stu-id="fd515-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="fd515-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="fd515-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="fd515-118">Cadeia de caracteres que consiste no nome do arquivo de um arquivo de fonte EUDC separado.</span><span class="sxs-lookup"><span data-stu-id="fd515-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="fd515-119">Esse arquivo identifica uma fonte a ser associada a TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="fd515-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="fd515-120">O exemplo a seguir mostra a chave EUDC para a página de código 932.</span><span class="sxs-lookup"><span data-stu-id="fd515-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="fd515-121">O exemplo a seguir define a fonte EUDC padrão do sistema como Eudc.ttf e associa as fontes EUDC separadas Mineudc.ttf e Goteudc.ttf aos nomes de fonte MS Mincho e MS Ques, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fd515-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="fd515-122">Quando a página de código do Windows (sistema ACP) associada à linguagem para programas não Unicode corresponde à sub-chave , o subsistema GDI procura os pares de valores de sub-chave para obter informações de exibição sobre o caractere.</span><span class="sxs-lookup"><span data-stu-id="fd515-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="fd515-123">Primeiro, ele procura um nome que corresponde à fonte atual.</span><span class="sxs-lookup"><span data-stu-id="fd515-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="fd515-124">Se não houver nenhum, ele examinará o valor SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="fd515-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="fd515-125">Se nenhum valor for definido, a GDI tratará o caractere como indefinido.</span><span class="sxs-lookup"><span data-stu-id="fd515-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="fd515-126">Observe que o texto em si não precisa estar na página de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="fd515-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="fd515-127">Por exemplo, suponha que a página de código tenha o identificador 1252, a página de código padrão do Windows para inglês.</span><span class="sxs-lookup"><span data-stu-id="fd515-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="fd515-128">Um aplicativo passa o único ponto de código Unicode U+E000, na PUA (área de uso privado Unicode), para [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext)</span><span class="sxs-lookup"><span data-stu-id="fd515-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="fd515-129">Nesse caso, a GDI analisa os valores do Registro em 1252 para obter as informações de fonte para as propriedades de exibição de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fd515-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd515-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd515-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd515-131">Entradas do Registro EUDC</span><span class="sxs-lookup"><span data-stu-id="fd515-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="fd515-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="fd515-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
