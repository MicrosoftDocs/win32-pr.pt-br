---
description: Vários factos descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisam ter formatos diferentes para idiomas diferentes. A tabela a seguir lista os factos que são comuns em todos os idiomas.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factos comuns entre linguagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814013"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="b907e-104">Factos comuns entre linguagens</span><span class="sxs-lookup"><span data-stu-id="b907e-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="b907e-105">Vários factos descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisam ter formatos diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="b907e-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="b907e-106">A tabela a seguir lista os factos que são comuns em todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="b907e-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b907e-107">Facto</span><span class="sxs-lookup"><span data-stu-id="b907e-107">Factoid</span></span></th>
<th><span data-ttu-id="b907e-108">Definição</span><span class="sxs-lookup"><span data-stu-id="b907e-108">Definition</span></span></th>
<th><span data-ttu-id="b907e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b907e-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b907e-110"><strong>Dígito</strong></span><span class="sxs-lookup"><span data-stu-id="b907e-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="b907e-111">Define a tendência de um único dígito.</span><span class="sxs-lookup"><span data-stu-id="b907e-111">Sets bias for a single digit.</span></span> <span data-ttu-id="b907e-112">O reconhecedor é polarizado para retornar apenas dígitos únicos quando esse factor é definido.</span><span class="sxs-lookup"><span data-stu-id="b907e-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="b907e-113">0-9</span><span class="sxs-lookup"><span data-stu-id="b907e-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b907e-114"><strong>Email</strong></span><span class="sxs-lookup"><span data-stu-id="b907e-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="b907e-115">Define a tendência de um endereço de email.</span><span class="sxs-lookup"><span data-stu-id="b907e-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b907e-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="b907e-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="b907e-117">Define a tendência para vários formatos de URL.</span><span class="sxs-lookup"><span data-stu-id="b907e-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b907e-118">As configurações padrão do reconhecedor incluem o facto <strong>da Web</strong> .</span><span class="sxs-lookup"><span data-stu-id="b907e-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="b907e-119">Por isso, você não pode notar uma grande diferença entre o facto <strong>da Web</strong> e a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="b907e-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="b907e-120">No entanto, o facto <strong>da Web</strong> ajuda a eliminar espaços entre palavras em uma URL.</span><span class="sxs-lookup"><span data-stu-id="b907e-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="b907e-121">http: \\ Microsoft.net</span><span class="sxs-lookup"><span data-stu-id="b907e-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="b907e-122">https: \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="b907e-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="b907e-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="b907e-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="b907e-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="b907e-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="b907e-125">http: \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="b907e-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="b907e-126">http: \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="b907e-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="b907e-127">http: \\ www. Microsoft. com\myfile.asp</span><span class="sxs-lookup"><span data-stu-id="b907e-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="b907e-128">http: \\ www.Microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="b907e-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="b907e-129">http: \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="b907e-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="b907e-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="b907e-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b907e-131"><strong>Padrão</strong></span><span class="sxs-lookup"><span data-stu-id="b907e-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="b907e-132">Retorna o reconhecedor às suas configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="b907e-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="b907e-133">A configuração padrão de factores para idiomas ocidentais inclui o dicionário do sistema, o dicionário do usuário, várias pontuações e as inicializações <strong>da Web</strong> e de <strong>número</strong> .</span><span class="sxs-lookup"><span data-stu-id="b907e-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="b907e-134">A configuração padrão para o factos para idiomas do leste asiático inclui todos os caracteres suportados pelo reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="b907e-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b907e-135"><strong>Nenhuma</strong></span><span class="sxs-lookup"><span data-stu-id="b907e-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="b907e-136">Desabilita todos os factos, dicionários e o modelo de linguagem.</span><span class="sxs-lookup"><span data-stu-id="b907e-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="b907e-137">Esse factor deve ser usado somente quando você não quiser que o reconhecedor Use quaisquer regras ou dicionários gramaticais, incluindo o dicionário do sistema.</span><span class="sxs-lookup"><span data-stu-id="b907e-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="b907e-138">Esse factor é útil para entrada de cadeias de caracteres aleatórias, como códigos de produto.</span><span class="sxs-lookup"><span data-stu-id="b907e-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="b907e-139">Não use o sinalizador de coerção com esse factor.</span><span class="sxs-lookup"><span data-stu-id="b907e-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




