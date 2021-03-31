---
title: GetStyle IAgentBalloonEx
description: GetStyle IAgentBalloonEx
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822823"
---
# <a name="iagentballoonexgetstyle"></a><span data-ttu-id="91974-103">IAgentBalloonEx:: GetStyle</span><span class="sxs-lookup"><span data-stu-id="91974-103">IAgentBalloonEx::GetStyle</span></span>

<span data-ttu-id="91974-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="91974-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

<span data-ttu-id="91974-105">Recupera as configurações de estilo de balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="91974-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="91974-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="91974-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="91974-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span><span class="sxs-lookup"><span data-stu-id="91974-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span></span>
</dt> <dd>

<span data-ttu-id="91974-108">Configurações de estilo para o balão do Word, que pode ser uma combinação de qualquer um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="91974-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="91974-109">Valor</span><span class="sxs-lookup"><span data-stu-id="91974-109">Value</span></span>                                                                           | <span data-ttu-id="91974-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="91974-110">Description</span></span>                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="91974-111">balão de estilo de balão **curto sem sinal const** **\_ \_ = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="91974-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/> | <span data-ttu-id="91974-112">O balão tem suporte para saída.</span><span class="sxs-lookup"><span data-stu-id="91974-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="91974-113">const estilo de balão **curto não assinado** **\_ \_ SIZETOTEXT = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="91974-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span>           | <span data-ttu-id="91974-114">A altura do balão é dimensionada para acomodar a saída do texto.</span><span class="sxs-lookup"><span data-stu-id="91974-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="91974-115">**const-** **AutoOcultar estilo de balão não assinado constante \_ \_ = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="91974-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span>            | <span data-ttu-id="91974-116">O balão é ocultado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91974-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="91974-117">**const não assinada estilo curto** de **balão \_ \_ autoritmo = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="91974-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span>            | <span data-ttu-id="91974-118">A saída do texto é peratualizada com base na taxa de saída.</span><span class="sxs-lookup"><span data-stu-id="91974-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="91974-119">Quando o bit do estilo de **balão** é definido, o balão de palavra é exibido quando o método [**Speak**](speak-method.md) ou [**Think**](think-method.md) é usado, a menos que o usuário substitua sua exibição por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="91974-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display through the Microsoft Agent property sheet.</span></span> <span data-ttu-id="91974-120">Quando não definido, nenhum balão é exibido.</span><span class="sxs-lookup"><span data-stu-id="91974-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="91974-121">Quando o bit do estilo **SizeToText** é definido, o balão do Word dimensiona automaticamente a altura do balão para o tamanho atual do texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="91974-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="91974-122">Quando não definido, a altura do balão é baseada na configuração da propriedade número de linhas do balão.</span><span class="sxs-lookup"><span data-stu-id="91974-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="91974-123">Esse bit de estilo é definido como 1 e uma tentativa de usar [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="91974-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="91974-124">Quando o bit do estilo de **AutoOcultar** é definido, o balão de palavras é ocultado automaticamente após um curto tempo limite. Quando não definido, o balão é exibido até uma nova chamada de [**fala**](speak-method.md) ou [**reflexão**](think-method.md) , o caractere é ocultado ou o usuário clica ou arrasta o caractere.</span><span class="sxs-lookup"><span data-stu-id="91974-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short time-out. When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="91974-125">Quando o bit do estilo do **autoritmo** é definido, o balão do Word ultrapassa a saída com base na taxa de saída atual, por exemplo, uma palavra por vez.</span><span class="sxs-lookup"><span data-stu-id="91974-125">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="91974-126">Quando a saída excede o tamanho do balão, o texto anterior é rolado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91974-126">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="91974-127">Quando não definido, todo o texto incluído em uma instrução de [**fala**](speak-method.md) ou de [**reflexão**](think-method.md) é exibido de uma vez.</span><span class="sxs-lookup"><span data-stu-id="91974-127">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="91974-128">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="91974-128">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="91974-129">Os padrões para esses bits de estilo se baseiam nas configurações quando o caractere é compilado por meio do editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="91974-129">The defaults for these style bits are based on the settings when the character is compiled through the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="91974-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="91974-130">See Also</span></span>

[<span data-ttu-id="91974-131">**IAgentBalloonEx:: SetStyle**</span><span class="sxs-lookup"><span data-stu-id="91974-131">**IAgentBalloonEx::SetStyle**</span></span>](iagentballoonex--setstyle.md)


 

 





