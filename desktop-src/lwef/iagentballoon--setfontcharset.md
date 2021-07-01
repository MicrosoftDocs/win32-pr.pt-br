---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120201"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="2b7e1-103">IAgentBallball::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="2b7e1-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="2b7e1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2b7e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="2b7e1-105">Define o conjunto de caracteres da fonte exibida na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="2b7e1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2b7e1-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="2b7e1-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="2b7e1-108">O conjunto de caracteres da fonte.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-108">The character set of the font.</span></span> <span data-ttu-id="2b7e1-109">Veja a seguir algumas configurações comuns de valor:</span><span class="sxs-lookup"><span data-stu-id="2b7e1-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="2b7e1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2b7e1-110">Value</span></span>    | <span data-ttu-id="2b7e1-111">Conjunto de caracteres</span><span class="sxs-lookup"><span data-stu-id="2b7e1-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7e1-112">0</span><span class="sxs-lookup"><span data-stu-id="2b7e1-112">0</span></span>   | <span data-ttu-id="2b7e1-113">CARACTEREs padrão do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2b7e1-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="2b7e1-114">1</span><span class="sxs-lookup"><span data-stu-id="2b7e1-114">1</span></span>   | <span data-ttu-id="2b7e1-115">Conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="2b7e1-116">2</span><span class="sxs-lookup"><span data-stu-id="2b7e1-116">2</span></span>   | <span data-ttu-id="2b7e1-117">O conjunto de caracteres de símbolo.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="2b7e1-118">128</span><span class="sxs-lookup"><span data-stu-id="2b7e1-118">128</span></span> | <span data-ttu-id="2b7e1-119">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em japonês do Windows.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="2b7e1-120">129</span><span class="sxs-lookup"><span data-stu-id="2b7e1-120">129</span></span> | <span data-ttu-id="2b7e1-121">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em coreano do Windows.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="2b7e1-122">134</span><span class="sxs-lookup"><span data-stu-id="2b7e1-122">134</span></span> | <span data-ttu-id="2b7e1-123">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão simplificada em chinês do Windows.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="2b7e1-124">136</span><span class="sxs-lookup"><span data-stu-id="2b7e1-124">136</span></span> | <span data-ttu-id="2b7e1-125">DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão tradicional em chinês do Windows.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="2b7e1-126">255</span><span class="sxs-lookup"><span data-stu-id="2b7e1-126">255</span></span> | <span data-ttu-id="2b7e1-127">Caracteres estendidos geralmente exibidos por aplicativos MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="2b7e1-128">Para outros valores de conjunto de caracteres, consulte a documentação do SDK da Plataforma.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="2b7e1-129">O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no Editor de Caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2b7e1-130">Você pode alterá-lo com [**IAgentBallball::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="2b7e1-130">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="2b7e1-131">No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="2b7e1-132">Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-132">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b7e1-133">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2b7e1-133">See Also</span></span>

[<span data-ttu-id="2b7e1-134">**IAgentBallball::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="2b7e1-134">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




