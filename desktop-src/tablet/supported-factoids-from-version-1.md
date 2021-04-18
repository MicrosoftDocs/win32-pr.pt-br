---
description: A plataforma do Tablet PC dá suporte a várias que são usadas para aumentar a precisão do reconhecimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factos com suporte da versão 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782210"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="f2d02-103">Factos com suporte da versão 1</span><span class="sxs-lookup"><span data-stu-id="f2d02-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="f2d02-104">\[Observe que a seguinte descrição das opções com suporte na versão 1 do SDK (Software Development Kit) do Microsoft Windows XP Tablet PC Edition ainda é suportada por reconhecedores, mas é recomendável que todo o novo desenvolvimento (para os reconhecedores do script Latin) Use os valores definidos na enumeração [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]</span><span class="sxs-lookup"><span data-stu-id="f2d02-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="f2d02-105">A plataforma do Tablet PC dá suporte a várias que são usadas para aumentar a precisão do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="f2d02-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="f2d02-106">Ao usar os factos, é importante que a entrada esperada corresponda exatamente à definição do factor.</span><span class="sxs-lookup"><span data-stu-id="f2d02-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="f2d02-107">Se a entrada não corresponder à definição do factor, a precisão do reconhecimento será prejudicada.</span><span class="sxs-lookup"><span data-stu-id="f2d02-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="f2d02-108">Por exemplo, se o factor de **número** for definido e o usuário inserir letras, a precisão de reconhecimento de letras será ruim.</span><span class="sxs-lookup"><span data-stu-id="f2d02-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="f2d02-109">Determinados factos, como **email** e **dígito**, são quase idênticos entre os idiomas.</span><span class="sxs-lookup"><span data-stu-id="f2d02-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="f2d02-110">Outros factos, como **telefone** e **PostalCode**, variam por idioma.</span><span class="sxs-lookup"><span data-stu-id="f2d02-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="f2d02-111">Examine o formato de cada factor para o idioma que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f2d02-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="f2d02-112">Uma lista de formatos para cada factor em cada idioma pode ser encontrada nas tabelas nos tópicos que seguem este tópico.</span><span class="sxs-lookup"><span data-stu-id="f2d02-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="f2d02-113">Há uma distinção sutil, mas importante, entre os factos para idiomas ocidentais e as para idiomas do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="f2d02-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="f2d02-114">Os factos para idiomas ocidentais são implementados usando expressões que descrevem o resultado desejado.</span><span class="sxs-lookup"><span data-stu-id="f2d02-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="f2d02-115">O reconhecedor é então polarizado para produzir resultados que correspondam a essa expressão.</span><span class="sxs-lookup"><span data-stu-id="f2d02-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="f2d02-116">As opções para idiomas do Leste Asiático são implementadas especificando um intervalo aceitável de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f2d02-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="f2d02-117">Por exemplo, o facto de **Data** para idiomas do leste asiático aceita somente caracteres Unicode em um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="f2d02-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="f2d02-118">Os factos para os idiomas ocidentais incluem para inglês (Reino Unido), inglês (Estados Unidos), francês, alemão e espanhol.</span><span class="sxs-lookup"><span data-stu-id="f2d02-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="f2d02-119">Os factos para os idiomas do leste asiático incluem o factos para chinês (simplificado), chinês (tradicional), japonês e coreano.</span><span class="sxs-lookup"><span data-stu-id="f2d02-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="f2d02-120">As seções a seguir mostram os formatos com suporte para cada factor em cada idioma:</span><span class="sxs-lookup"><span data-stu-id="f2d02-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="f2d02-121">Factos comuns entre linguagens</span><span class="sxs-lookup"><span data-stu-id="f2d02-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="f2d02-122">Factos para idiomas ocidentais</span><span class="sxs-lookup"><span data-stu-id="f2d02-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="f2d02-123">Factos para idiomas do leste asiático</span><span class="sxs-lookup"><span data-stu-id="f2d02-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="f2d02-124">Se você esperar uma entrada diferente dos formatos listados nas tabelas nessas seções, não use um factor.</span><span class="sxs-lookup"><span data-stu-id="f2d02-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="f2d02-125">Além disso, os factos são incorporados ao reconhecedor para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="f2d02-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="f2d02-126">Você não pode usar os factos de um idioma com um reconhecedor de outro idioma.</span><span class="sxs-lookup"><span data-stu-id="f2d02-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="f2d02-127">Por exemplo, você não pode usar o botão de **telefone** francês com um reconhecedor japonês.</span><span class="sxs-lookup"><span data-stu-id="f2d02-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2d02-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2d02-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2d02-129">**Constantes do factor**</span><span class="sxs-lookup"><span data-stu-id="f2d02-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="f2d02-130">[Classe Microsoft. Ink. Factoname](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f2d02-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
