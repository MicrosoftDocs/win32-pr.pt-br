---
description: O serviço de detecção de idioma ELS é chamado de Microsoft Detecção de Idioma. Esse serviço usa a tecnologia patenteada pela Microsoft para permitir que os aplicativos detectem o idioma no qual o texto específico é escrito.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Detecção de Idioma da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785442"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="b81e3-104">Detecção de Idioma da Microsoft</span><span class="sxs-lookup"><span data-stu-id="b81e3-104">Microsoft Language Detection</span></span>

<span data-ttu-id="b81e3-105">O serviço de detecção de idioma ELS é chamado de Microsoft Detecção de Idioma.</span><span class="sxs-lookup"><span data-stu-id="b81e3-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="b81e3-106">Esse serviço usa a tecnologia patenteada pela Microsoft para permitir que os aplicativos detectem o idioma no qual o texto específico é escrito.</span><span class="sxs-lookup"><span data-stu-id="b81e3-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="b81e3-107">Entrada para o Microsoft Detecção de Idioma</span><span class="sxs-lookup"><span data-stu-id="b81e3-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="b81e3-108">A entrada para o serviço Microsoft Detecção de Idioma é texto UTF-16 (forma normalizada C).</span><span class="sxs-lookup"><span data-stu-id="b81e3-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="b81e3-109">O serviço precisa determinar o idioma deste texto.</span><span class="sxs-lookup"><span data-stu-id="b81e3-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="b81e3-110">Saída do Microsoft Detecção de Idioma</span><span class="sxs-lookup"><span data-stu-id="b81e3-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="b81e3-111">O serviço de Detecção de Idioma da Microsoft recupera as linguagens de listagem de cadeias de caracteres UTF-16 com final de nulo, representadas por seus nomes, separadas por delimitadores de caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="b81e3-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="b81e3-112">A lista é classificada por relevância.</span><span class="sxs-lookup"><span data-stu-id="b81e3-112">The list is sorted by relevance.</span></span> <span data-ttu-id="b81e3-113">Para a maioria dos idiomas, são usados nomes neutros.</span><span class="sxs-lookup"><span data-stu-id="b81e3-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="b81e3-114">No entanto, para alguns, por exemplo, Sr-Cyrl, sr-latn, zh-Hant e zh-Hans, os nomes completos são usados.</span><span class="sxs-lookup"><span data-stu-id="b81e3-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="b81e3-115">Operação do Microsoft Detecção de Idioma</span><span class="sxs-lookup"><span data-stu-id="b81e3-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="b81e3-116">O serviço Microsoft Detecção de Idioma verifica o script Unicode do texto fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b81e3-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="b81e3-117">Ele segmenta o texto com base nos scripts que detecta e determina o idioma no qual cada segmento é gravado.</span><span class="sxs-lookup"><span data-stu-id="b81e3-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="b81e3-118">Se um script indicar um único idioma, a linguagem terá a garantia de estar presente na lista de saída de idiomas.</span><span class="sxs-lookup"><span data-stu-id="b81e3-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="b81e3-119">O serviço usa um algoritmo patenteado para determinar a relevância de cada idioma com suporte.</span><span class="sxs-lookup"><span data-stu-id="b81e3-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="b81e3-120">GUID do Microsoft Detecção de Idioma</span><span class="sxs-lookup"><span data-stu-id="b81e3-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="b81e3-121">O GUID para o serviço Microsoft Detecção de Idioma é declarado em Elssrvc. h, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b81e3-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="b81e3-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b81e3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b81e3-123">Sobre os serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="b81e3-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



