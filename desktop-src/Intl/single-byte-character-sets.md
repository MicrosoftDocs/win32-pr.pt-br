---
description: Um SBCS (conjunto de caracteres de byte único) é um mapeamento de 256 caracteres individuais para seus valores de código de identificação, implementados como uma página de código.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Conjuntos de caracteres de byte único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922822"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="1c737-103">Conjuntos de caracteres de byte único</span><span class="sxs-lookup"><span data-stu-id="1c737-103">Single-byte Character Sets</span></span>

<span data-ttu-id="1c737-104">Um SBCS (conjunto de caracteres de byte único) é um mapeamento de 256 caracteres individuais para seus valores de código de identificação, implementados como uma página de código.</span><span class="sxs-lookup"><span data-stu-id="1c737-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="1c737-105">Um SBCS pode corresponder a uma página de código do Windows ou a uma página de código OEM.</span><span class="sxs-lookup"><span data-stu-id="1c737-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="1c737-106">Uma página de código SBCS também pode incluir uma página de código não nativa, por exemplo, uma página de código EBCDIC.</span><span class="sxs-lookup"><span data-stu-id="1c737-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="1c737-107">Para obter definições dessas páginas de código, consulte [páginas de código](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="1c737-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="1c737-108">Novos aplicativos do Windows devem usar [Unicode](unicode.md) para evitar as inconsistências de páginas de código variadas e para facilitar a localização.</span><span class="sxs-lookup"><span data-stu-id="1c737-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="1c737-109">No entanto, alguns protocolos herdados exigem o uso de um SBCS.</span><span class="sxs-lookup"><span data-stu-id="1c737-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="1c737-110">Cada página de código SBCS dá suporte a caracteres diferentes, mas nenhuma página dá suporte a toda a amplitude de caracteres fornecida pelo Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c737-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="1c737-111">Cada página de código SBCS dá suporte a um subconjunto diferente, codificado de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="1c737-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="1c737-112">Os dados convertidos de uma página de código SBCS para outra estão sujeitos a corrupção, pois o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente.</span><span class="sxs-lookup"><span data-stu-id="1c737-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="1c737-113">Os dados convertidos de Unicode para SBCS estão sujeitos à perda de dados porque uma determinada página de código pode não ser capaz de representar todos os caracteres usados nesses dados Unicode específicos.</span><span class="sxs-lookup"><span data-stu-id="1c737-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="1c737-114">Seus aplicativos usam páginas de código do Windows SBCS com as versões "A" do Windows functions.</span><span class="sxs-lookup"><span data-stu-id="1c737-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="1c737-115">Consulte [convenções para protótipos de função](conventions-for-function-prototypes.md) e [páginas de código](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="1c737-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="1c737-116">Para ajudar a identificar uma página de código SBCS, um aplicativo pode usar a função [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="1c737-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="1c737-117">Além disso, um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para mapear entre cadeias de caracteres Unicode e SBCS.</span><span class="sxs-lookup"><span data-stu-id="1c737-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c737-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c737-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c737-119">Conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="1c737-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="1c737-120">Conjuntos de caracteres de byte duplo</span><span class="sxs-lookup"><span data-stu-id="1c737-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



