---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120401"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="9fd5b-103">IAgentBallball::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="9fd5b-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="9fd5b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9fd5b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="9fd5b-105">Indica o conjunto de caracteres da fonte exibida em um balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="9fd5b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9fd5b-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="9fd5b-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="9fd5b-108">O endereço de um valor que recebe o conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="9fd5b-109">Veja a seguir algumas configurações comuns de valor:</span><span class="sxs-lookup"><span data-stu-id="9fd5b-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="9fd5b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9fd5b-110">Value</span></span>    | <span data-ttu-id="9fd5b-111">Conjunto de caracteres</span><span class="sxs-lookup"><span data-stu-id="9fd5b-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd5b-112">0</span><span class="sxs-lookup"><span data-stu-id="9fd5b-112">0</span></span>   | <span data-ttu-id="9fd5b-113">CARACTEREs padrão do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="9fd5b-114">1</span><span class="sxs-lookup"><span data-stu-id="9fd5b-114">1</span></span>   | <span data-ttu-id="9fd5b-115">Conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="9fd5b-116">2</span><span class="sxs-lookup"><span data-stu-id="9fd5b-116">2</span></span>   | <span data-ttu-id="9fd5b-117">O conjunto de caracteres de símbolo.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="9fd5b-118">128</span><span class="sxs-lookup"><span data-stu-id="9fd5b-118">128</span></span> | <span data-ttu-id="9fd5b-119">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em japonês do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="9fd5b-120">129</span><span class="sxs-lookup"><span data-stu-id="9fd5b-120">129</span></span> | <span data-ttu-id="9fd5b-121">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em coreano do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="9fd5b-122">134</span><span class="sxs-lookup"><span data-stu-id="9fd5b-122">134</span></span> | <span data-ttu-id="9fd5b-123">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão simplificada em chinês do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="9fd5b-124">136</span><span class="sxs-lookup"><span data-stu-id="9fd5b-124">136</span></span> | <span data-ttu-id="9fd5b-125">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão tradicional em chinês do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="9fd5b-126">255</span><span class="sxs-lookup"><span data-stu-id="9fd5b-126">255</span></span> | <span data-ttu-id="9fd5b-127">Caracteres estendidos geralmente exibidos por aplicativos MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="9fd5b-128">Para outros valores de conjunto de caracteres, consulte a documentação do SDK da Plataforma.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="9fd5b-129">O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no Editor de Caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9fd5b-130">Você pode alterá-lo [**usando IAgentBallball::SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="9fd5b-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="9fd5b-131">No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9fd5b-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fd5b-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9fd5b-132">See Also</span></span>

[<span data-ttu-id="9fd5b-133">**IAgentBallball::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="9fd5b-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




