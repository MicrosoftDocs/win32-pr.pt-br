---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159986"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="743cd-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="743cd-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="743cd-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="743cd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="743cd-105">Indica o conjunto de caracteres da fonte exibida em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="743cd-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="743cd-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="743cd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="743cd-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="743cd-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="743cd-108">O endereço de um valor que recebe o conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="743cd-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="743cd-109">A seguir estão algumas configurações comuns para o valor:</span><span class="sxs-lookup"><span data-stu-id="743cd-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="743cd-110">0</span><span class="sxs-lookup"><span data-stu-id="743cd-110">0</span></span>   | <span data-ttu-id="743cd-111">Caracteres padrão do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="743cd-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="743cd-112">1</span><span class="sxs-lookup"><span data-stu-id="743cd-112">1</span></span>   | <span data-ttu-id="743cd-113">Conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="743cd-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="743cd-114">2</span><span class="sxs-lookup"><span data-stu-id="743cd-114">2</span></span>   | <span data-ttu-id="743cd-115">O conjunto de caracteres do símbolo.</span><span class="sxs-lookup"><span data-stu-id="743cd-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="743cd-116">128</span><span class="sxs-lookup"><span data-stu-id="743cd-116">128</span></span> | <span data-ttu-id="743cd-117">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão japonesa do Windows.</span><span class="sxs-lookup"><span data-stu-id="743cd-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="743cd-118">129</span><span class="sxs-lookup"><span data-stu-id="743cd-118">129</span></span> | <span data-ttu-id="743cd-119">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão coreana do Windows.</span><span class="sxs-lookup"><span data-stu-id="743cd-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="743cd-120">134</span><span class="sxs-lookup"><span data-stu-id="743cd-120">134</span></span> | <span data-ttu-id="743cd-121">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão do Windows em chinês simplificado.</span><span class="sxs-lookup"><span data-stu-id="743cd-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="743cd-122">136</span><span class="sxs-lookup"><span data-stu-id="743cd-122">136</span></span> | <span data-ttu-id="743cd-123">DBCS (conjunto de caracteres de dois bytes) exclusivo da versão em Chinês tradicional do Windows.</span><span class="sxs-lookup"><span data-stu-id="743cd-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="743cd-124">255</span><span class="sxs-lookup"><span data-stu-id="743cd-124">255</span></span> | <span data-ttu-id="743cd-125">Caracteres estendidos geralmente exibidos por aplicativos do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="743cd-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="743cd-126">Para outros valores de conjunto de caracteres, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="743cd-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="743cd-127">O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="743cd-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="743cd-128">Você pode alterá-lo usando [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="743cd-128">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="743cd-129">No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="743cd-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="743cd-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="743cd-130">See Also</span></span>

[<span data-ttu-id="743cd-131">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="743cd-131">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




