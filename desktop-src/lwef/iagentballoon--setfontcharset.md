---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793314"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="1b632-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="1b632-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="1b632-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1b632-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="1b632-105">Define o conjunto de caracteres da fonte exibida na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="1b632-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="1b632-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1b632-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1b632-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="1b632-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="1b632-108">O conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="1b632-108">The character set of the font.</span></span> <span data-ttu-id="1b632-109">A seguir estão algumas configurações comuns para o valor:</span><span class="sxs-lookup"><span data-stu-id="1b632-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b632-110">0</span><span class="sxs-lookup"><span data-stu-id="1b632-110">0</span></span>   | <span data-ttu-id="1b632-111">Caracteres padrão do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="1b632-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="1b632-112">1</span><span class="sxs-lookup"><span data-stu-id="1b632-112">1</span></span>   | <span data-ttu-id="1b632-113">Conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="1b632-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="1b632-114">2</span><span class="sxs-lookup"><span data-stu-id="1b632-114">2</span></span>   | <span data-ttu-id="1b632-115">O conjunto de caracteres do símbolo.</span><span class="sxs-lookup"><span data-stu-id="1b632-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="1b632-116">128</span><span class="sxs-lookup"><span data-stu-id="1b632-116">128</span></span> | <span data-ttu-id="1b632-117">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão japonesa do Windows.</span><span class="sxs-lookup"><span data-stu-id="1b632-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="1b632-118">129</span><span class="sxs-lookup"><span data-stu-id="1b632-118">129</span></span> | <span data-ttu-id="1b632-119">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão coreana do Windows.</span><span class="sxs-lookup"><span data-stu-id="1b632-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="1b632-120">134</span><span class="sxs-lookup"><span data-stu-id="1b632-120">134</span></span> | <span data-ttu-id="1b632-121">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão do Windows em chinês simplificado.</span><span class="sxs-lookup"><span data-stu-id="1b632-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="1b632-122">136</span><span class="sxs-lookup"><span data-stu-id="1b632-122">136</span></span> | <span data-ttu-id="1b632-123">DBCS (conjunto de caracteres de dois bytes) exclusivo da versão em Chinês tradicional do Windows.</span><span class="sxs-lookup"><span data-stu-id="1b632-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="1b632-124">255</span><span class="sxs-lookup"><span data-stu-id="1b632-124">255</span></span> | <span data-ttu-id="1b632-125">Caracteres estendidos geralmente exibidos por aplicativos do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="1b632-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="1b632-126">Para outros valores de conjunto de caracteres, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="1b632-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="1b632-127">O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1b632-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1b632-128">Você pode alterá-lo com [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="1b632-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="1b632-129">No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1b632-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="1b632-130">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1b632-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b632-131">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1b632-131">See Also</span></span>

[<span data-ttu-id="1b632-132">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="1b632-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




