---
title: Marcas de saída de fala do Microsoft Agent
description: Marcas de saída de fala do Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822666"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="6d7db-103">Marcas de saída de fala do Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="6d7db-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="6d7db-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d7db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6d7db-105">Os serviços do Microsoft Agent dão suporte à modificação da saída de fala por meio de marcas especiais inseridas na cadeia de texto de fala.</span><span class="sxs-lookup"><span data-stu-id="6d7db-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="6d7db-106">Essas marcas ajudam a alterar as características da expressão de saída do caractere.</span><span class="sxs-lookup"><span data-stu-id="6d7db-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="6d7db-107">As marcas de saída de fala usam as seguintes regras de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6d7db-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="6d7db-108">Todas as marcas começam e terminam com um caractere de barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="6d7db-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="6d7db-109">O caractere de barra invertida simples não está habilitado dentro de uma marca.</span><span class="sxs-lookup"><span data-stu-id="6d7db-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="6d7db-110">Para incluir um caractere de barra invertida em um parâmetro de texto de uma marca, use uma barra invertida dupla ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="6d7db-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="6d7db-111">As marcas não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6d7db-111">Tags are case-insensitive.</span></span> <span data-ttu-id="6d7db-112">Por exemplo, \\ \\ o Pit é o mesmo que o \\ Pit \\ .</span><span class="sxs-lookup"><span data-stu-id="6d7db-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="6d7db-113">As marcas são dependentes de espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="6d7db-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="6d7db-114">Por exemplo, \\ RST \\ não é o mesmo que \\ RST \\ .</span><span class="sxs-lookup"><span data-stu-id="6d7db-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="6d7db-115">A menos que especificado em contrário ou modificado por outra marca, a saída de fala retém a característica definida pela marca dentro do texto especificado em um único método de [**fala**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6d7db-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="6d7db-116">A saída de fala é redefinida automaticamente por meio dos parâmetros definidos pelo usuário depois que um método de **fala** é concluído.</span><span class="sxs-lookup"><span data-stu-id="6d7db-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="6d7db-117">Algumas marcas incluem cadeias de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="6d7db-117">Some tags include quoted strings.</span></span> <span data-ttu-id="6d7db-118">Para algumas linguagens de programação, como Visual Basic Scripting Edition (VBScript) e Visual Basic, isso significa que você pode precisar usar duas aspas para designar o parâmetro da marca ou concatenar um caractere de aspas duplas como parte da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d7db-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="6d7db-119">O último é mostrado neste Visual Basic exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d7db-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="6d7db-120">Para C, C++ e Java™ programação, preceda as barras invertidas e aspas duplas com uma barra invertida.</span><span class="sxs-lookup"><span data-stu-id="6d7db-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="6d7db-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6d7db-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="6d7db-122">Para idiomas estrangeiros que dão suporte a caracteres DBCS (conjunto de caracteres de dois bytes), você pode usar caracteres de byte duplo para especificar parâmetros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d7db-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="6d7db-123">No entanto, use caracteres de byte único para todos os outros parâmetros e caracteres que são usados para definir a marca, incluindo a marca em si.</span><span class="sxs-lookup"><span data-stu-id="6d7db-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="6d7db-124">Há suporte para as seguintes marcas:</span><span class="sxs-lookup"><span data-stu-id="6d7db-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="6d7db-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="6d7db-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="6d7db-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="6d7db-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="6d7db-127">**EMP**</span><span class="sxs-lookup"><span data-stu-id="6d7db-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="6d7db-128">**Ficheiro**</span><span class="sxs-lookup"><span data-stu-id="6d7db-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="6d7db-129">**Mapeamento**</span><span class="sxs-lookup"><span data-stu-id="6d7db-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="6d7db-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="6d7db-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="6d7db-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="6d7db-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="6d7db-132">**Poço**</span><span class="sxs-lookup"><span data-stu-id="6d7db-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="6d7db-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="6d7db-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="6d7db-134">**SPD**</span><span class="sxs-lookup"><span data-stu-id="6d7db-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="6d7db-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="6d7db-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="6d7db-136">As marcas são projetadas principalmente para ajustar a saída gerada por conversão de texto em fala (TTS).</span><span class="sxs-lookup"><span data-stu-id="6d7db-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="6d7db-137">Somente as marcas [**mrk**](mrk-tag.md) e [**MAP**](map-tag.md) podem ser usadas com saída falada com base em arquivo de som.</span><span class="sxs-lookup"><span data-stu-id="6d7db-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="6d7db-138">O Microsoft Agent não oferece suporte a todas as marcas documentadas no SDK do Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="6d7db-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="6d7db-139">Os parâmetros também podem variar dependendo do mecanismo de TTS selecionado.</span><span class="sxs-lookup"><span data-stu-id="6d7db-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="6d7db-140">Você pode definir um mecanismo de TTS específico usando [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="6d7db-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




