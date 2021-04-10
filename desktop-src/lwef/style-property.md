---
title: Propriedade de estilo
description: Propriedade de estilo
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292207"
---
# <a name="style-property"></a><span data-ttu-id="8cb6b-103">Propriedade de estilo</span><span class="sxs-lookup"><span data-stu-id="8cb6b-103">Style Property</span></span>

<span data-ttu-id="8cb6b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8cb6b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8cb6b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="8cb6b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8cb6b-106">Retorna ou define o estilo de saída do balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="8cb6b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="8cb6b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8cb6b-108">\*agente do. ***Caracteres ("*** characterid \* \* *"). Estilo de balão. estilo* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="8cb6b-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="8cb6b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8cb6b-109">Part</span></span>    | <span data-ttu-id="8cb6b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cb6b-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb6b-111">*Estilo*</span><span class="sxs-lookup"><span data-stu-id="8cb6b-111">*Style*</span></span> | <span data-ttu-id="8cb6b-112">Um inteiro que representa o estilo de saída do balão.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="8cb6b-113">A configuração de estilo é um teletexto com bits correspondente a: balão (bit 0), tamanho-para-texto (bit 1), ocultar automaticamente (bit 2), auto-ritmo (bit 3), número de caracteres por linhas (bits 16-23) e número de linhas (bits 24-31).</span><span class="sxs-lookup"><span data-stu-id="8cb6b-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb6b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cb6b-114">Remarks</span></span>

<span data-ttu-id="8cb6b-115">Quando o bit de estilo de balão é definido como 1, o balão de palavra é exibido quando um método [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Think**](think-method.md) é usado, a menos que o usuário substitua essa configuração na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="8cb6b-116">Quando definido como 0, um balão não é exibido.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="8cb6b-117">Quando o bit do estilo de tamanho para texto é definido como 1, a palavra balão dimensiona automaticamente a altura do balão para o tamanho atual do texto da instrução [**Speak**](https://www.bing.com/search?q=**Speak**) ou [**Think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb6b-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="8cb6b-118">Quando definido como 0, a altura do balão é baseada na configuração da propriedade [**NumberOfLines**](numberoflines-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb6b-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="8cb6b-119">Se esse bit de estilo for definido como 1 e você tentar definir a propriedade **NumberOfLines** , o Agent gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="8cb6b-120">Quando o bit de estilo de ocultar automaticamente é definido como 1, o balão de palavras é ocultado automaticamente quando a saída falada é concluída.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="8cb6b-121">Quando definido como 0, o balão permanece exibido até a próxima chamada de [**fala**](https://www.bing.com/search?q=**Speak**) ou [**reflexão**](think-method.md) , o caractere é ocultado ou o usuário clica ou arrasta o caractere.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="8cb6b-122">Quando o bit de estilo do ritmo automático é definido como 1, o balão do Word ultrapassa a saída com base na taxa de saída atual, por exemplo, uma palavra de cada vez.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="8cb6b-123">Quando a saída excede o tamanho do balão, o texto anterior é rolado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="8cb6b-124">Quando definido como 0, todo o texto incluído em uma instrução de [**fala**](https://www.bing.com/search?q=**Speak**) ou [**reflexão**](think-method.md) é exibido ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="8cb6b-125">Para recuperar apenas o valor dos quatro bits inferiores **e** o valor retornado pelo **estilo** com 255.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="8cb6b-126">Para definir um valor de bit **ou** o valor retornado com o valor do bits que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="8cb6b-127">Para desativar um bit **e** o valor retornado com um complemento do bit:</span><span class="sxs-lookup"><span data-stu-id="8cb6b-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="8cb6b-128">A propriedade **Style** também retorna o número de caracteres por linha no byte inferior da palavra superior e o número de linhas no grande byte da palavra superior.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="8cb6b-129">Embora isso possa ser lido com mais facilidade usando as propriedades [**CharsPerLine**](charsperline-property.md) e [**NumberOfLines**](numberoflines-property.md), a propriedade **Style** também permite que você defina esses valores.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="8cb6b-130">Por exemplo, para alterar o número de linhas, desmarque bits 24 para 31 com uma operação **and** lógica antes de definir o novo valor como o produto do novo valor vezes 2 ^ 24, adicionado ao valor existente da propriedade **Style** .</span><span class="sxs-lookup"><span data-stu-id="8cb6b-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="8cb6b-131">Para definir o número de caracteres por linha, limpe os bits 16 a 23 com uma operação **and** lógica antes de definir o novo valor como o produto do novo valor vezes 2 ^ 16, adicionado ao valor existente da Propriedade Style.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="8cb6b-132">A propriedade de **estilo** pode ser definida mesmo que o usuário tenha desabilitado a exibição de balão usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="8cb6b-133">No entanto, os valores para o número de linhas devem estar entre 1 e 128 e o número de caracteres por linha deve estar entre 8 e 255.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="8cb6b-134">Se você fornecer um valor inválido para a propriedade **Style** , o Agent gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="8cb6b-135">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="8cb6b-136">Os padrões para esses bits de estilo se baseiam em suas configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8cb6b-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




