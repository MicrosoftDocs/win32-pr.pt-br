---
title: Marcas de saída de fala do Microsoft Agent
description: Marcas de saída de fala do Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386795"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="e9f48-103">Marcas de saída de fala do Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="e9f48-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="e9f48-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9f48-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e9f48-105">Os serviços do Microsoft Agent suportam a modificação da saída de fala por meio de marcas especiais inseridas na cadeia de caracteres de texto de fala.</span><span class="sxs-lookup"><span data-stu-id="e9f48-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="e9f48-106">Essas marcas ajudam você a alterar as características da expressão de saída do caractere.</span><span class="sxs-lookup"><span data-stu-id="e9f48-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="e9f48-107">As marcas de saída de fala usam as seguintes regras de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="e9f48-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="e9f48-108">Todas as marcas começam e terminam com um caractere de faixa invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e9f48-108">All tags begin and end with a backslash character (\\).</span></span>
-   <span data-ttu-id="e9f48-109">O caractere de faixa invertida única não está habilitado em uma marca.</span><span class="sxs-lookup"><span data-stu-id="e9f48-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="e9f48-110">Para incluir um caractere de faixa invertida em um parâmetro de texto de uma marca, use uma faixa invertida dupla ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="e9f48-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\\).</span></span>
-   <span data-ttu-id="e9f48-111">As marcas não são sensíveis a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e9f48-111">Tags are case-insensitive.</span></span> <span data-ttu-id="e9f48-112">Por exemplo, \\ pit é o mesmo que PIT \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="e9f48-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="e9f48-113">As marcas são dependentes de espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="e9f48-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="e9f48-114">Por exemplo, \\ Rst \\ não é o mesmo que \\ Rst \\ .</span><span class="sxs-lookup"><span data-stu-id="e9f48-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="e9f48-115">A menos que especificado ou modificado de outra marca, a saída de fala retém a característica definida pela marca dentro do texto especificado em um único [**método Speak.**](speak-method.md)</span><span class="sxs-lookup"><span data-stu-id="e9f48-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="e9f48-116">A saída de fala é redefinida automaticamente por meio dos parâmetros definidos pelo usuário depois que um **método Speak** é concluído.</span><span class="sxs-lookup"><span data-stu-id="e9f48-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="e9f48-117">Algumas marcas incluem cadeias de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="e9f48-117">Some tags include quoted strings.</span></span> <span data-ttu-id="e9f48-118">Para algumas linguagens de programação, como Visual Basic Scripting Edition (VBScript) e Visual Basic, isso significa que você pode ter que usar duas aspas para designar o parâmetro da marca ou concatenar um caractere de aspas duplas como parte da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e9f48-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="e9f48-119">O último é mostrado neste Visual Basic exemplo:</span><span class="sxs-lookup"><span data-stu-id="e9f48-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="e9f48-120">Para programação C, C++e Java™, preceda aspas invertida e aspas duplas com uma faixa invertida.</span><span class="sxs-lookup"><span data-stu-id="e9f48-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="e9f48-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e9f48-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="e9f48-122">Para linguagens estrangeiras que suportam caracteres DBCS (conjunto de caracteres de byte duplo), você pode usar caracteres de byte duplo para especificar parâmetros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e9f48-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="e9f48-123">No entanto, use caracteres de byte único para todos os outros parâmetros e caracteres usados para definir a marca, incluindo a marca em si.</span><span class="sxs-lookup"><span data-stu-id="e9f48-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="e9f48-124">Há suporte para as seguintes marcas:</span><span class="sxs-lookup"><span data-stu-id="e9f48-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="e9f48-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="e9f48-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="e9f48-126">**Ctx**</span><span class="sxs-lookup"><span data-stu-id="e9f48-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="e9f48-127">**Emp**</span><span class="sxs-lookup"><span data-stu-id="e9f48-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="e9f48-128">**Lst**</span><span class="sxs-lookup"><span data-stu-id="e9f48-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="e9f48-129">**Mapa**</span><span class="sxs-lookup"><span data-stu-id="e9f48-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="e9f48-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="e9f48-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="e9f48-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="e9f48-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="e9f48-132">**Poço**</span><span class="sxs-lookup"><span data-stu-id="e9f48-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="e9f48-133">**Rst**</span><span class="sxs-lookup"><span data-stu-id="e9f48-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="e9f48-134">**Spd**</span><span class="sxs-lookup"><span data-stu-id="e9f48-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="e9f48-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="e9f48-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="e9f48-136">As marcas são projetadas principalmente para ajustar a saída gerada por TTS (texto em fala).</span><span class="sxs-lookup"><span data-stu-id="e9f48-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="e9f48-137">Somente as [**marcas Mrk**](mrk-tag.md) e [**Map**](map-tag.md) podem ser usadas com saída falada baseada em arquivo de som.</span><span class="sxs-lookup"><span data-stu-id="e9f48-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="e9f48-138">O Microsoft Agent não dá suporte a todas as marcas documentadas no SDK de Fala da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e9f48-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="e9f48-139">Os parâmetros também podem variar dependendo do mecanismo TTS selecionado.</span><span class="sxs-lookup"><span data-stu-id="e9f48-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="e9f48-140">Você pode definir um mecanismo TTS específico usando [**TTSModeID.**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="e9f48-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




