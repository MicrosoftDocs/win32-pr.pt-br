---
title: IAgentCharacterEx think
description: IAgentCharacterEx think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007452"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="36289-103">IAgentCharacterEx:: think</span><span class="sxs-lookup"><span data-stu-id="36289-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="36289-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36289-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="36289-105">Exibe o balão de palavras pensadas do caractere com o texto especificado.</span><span class="sxs-lookup"><span data-stu-id="36289-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="36289-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="36289-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="36289-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="36289-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="36289-108">O texto a ser exibido no balão de pensamento do caractere.</span><span class="sxs-lookup"><span data-stu-id="36289-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="36289-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="36289-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="36289-110">Endereço de uma variável que recebe a ID da solicitação de **reflexão** .</span><span class="sxs-lookup"><span data-stu-id="36289-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="36289-111">Assim como o método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , o método **Think** é uma solicitação em fila que exibe o texto em um balão de palavras, exceto que as ideias são exibidas em um balão de pensamento especial.</span><span class="sxs-lookup"><span data-stu-id="36289-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="36289-112">O balão de pensamento dá suporte apenas à marca de controle de fala de indicador (**\\ mrk**) e ignora quaisquer outras marcas de controle de fala.</span><span class="sxs-lookup"><span data-stu-id="36289-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="36289-113">Ao contrário de **IAgentCharacter:: Speak**, o método **Think** não altera o estado de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="36289-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="36289-114">As configurações de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) também se aplicam ao estilo de aparência do balão de pensamento.</span><span class="sxs-lookup"><span data-stu-id="36289-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="36289-115">Por exemplo, a propriedade [**habilitada**](enabled-property.md) do balão também deve ser **verdadeira** para o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="36289-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="36289-116">A quebra automática de palavras do Microsoft Agent no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço e tabulação).</span><span class="sxs-lookup"><span data-stu-id="36289-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="36289-117">No entanto, ele pode quebrar uma palavra para se ajustar também ao balão.</span><span class="sxs-lookup"><span data-stu-id="36289-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="36289-118">Em linguagens como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.</span><span class="sxs-lookup"><span data-stu-id="36289-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="36289-119">Defina a ID de idioma do caractere (usando [**IAgentCharacterEx:: Setlanguageid**](iagentcharacterex--setlanguageid.md) antes de usar o método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) para garantir a exibição de texto apropriada dentro do balão do Word.</span><span class="sxs-lookup"><span data-stu-id="36289-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="36289-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="36289-120">See Also</span></span>

<span data-ttu-id="36289-121">[**IAgentBalloon:: Gethabilited**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="36289-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 