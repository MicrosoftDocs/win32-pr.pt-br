---
title: IAgentCommand setvoice
description: IAgentCommand setvoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105782662"
---
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="8d611-103">IAgentCommand:: setvoice</span><span class="sxs-lookup"><span data-stu-id="8d611-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="8d611-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d611-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="8d611-105">Define a propriedade de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="8d611-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="8d611-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8d611-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8d611-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="8d611-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="8d611-108">Um BSTR que especifica o texto para a propriedade de [**voz**](voice-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="8d611-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="8d611-109">Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade de [**voz**](voice-property.md) e a propriedade [**habilitada**](enabled-property.md) definida como sendo acessível por voz.</span><span class="sxs-lookup"><span data-stu-id="8d611-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="8d611-110">Ele também deve ter sua propriedade [**VoiceCaption**](voicecaption-property.md) definida para aparecer na **janela de comandos de voz**.</span><span class="sxs-lookup"><span data-stu-id="8d611-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="8d611-111">(Para compatibilidade com versões anteriores, se não houver nenhum **VoiceCaption**, a configuração de [**legenda**](caption-property.md) será usada.)</span><span class="sxs-lookup"><span data-stu-id="8d611-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="8d611-112">A expressão BSTR que você fornece pode incluir caracteres de colchete ( \[ \] ) para indicar palavras opcionais e caracteres de barra vertical ( \| ) para indicar cadeias alternativas.</span><span class="sxs-lookup"><span data-stu-id="8d611-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="8d611-113">As alternativas devem ser colocadas entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="8d611-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="8d611-114">Por exemplo, "(Olá \[ \] \| , Oi Olá)" diz ao mecanismo de fala para aceitar "Olá", "Olá", "ou" Olá "para o comando.</span><span class="sxs-lookup"><span data-stu-id="8d611-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="8d611-115">Lembre-se de incluir os espaços apropriados entre o texto entre colchetes ou parênteses e o texto que não está entre colchetes ou parênteses.</span><span class="sxs-lookup"><span data-stu-id="8d611-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="8d611-116">Você pode usar o operador Star ( \* ) para especificar zero ou mais instâncias das palavras incluídas no grupo ou o operador de adição (+) para especificar uma ou mais instâncias.</span><span class="sxs-lookup"><span data-stu-id="8d611-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="8d611-117">Por exemplo, os seguintes resultados em uma gramática que dá suporte a "Experimente isto", "Tente isso" e "Tente isso", com iterações ilimitadas de "favor":</span><span class="sxs-lookup"><span data-stu-id="8d611-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="8d611-118">O seguinte formato de gramática exclui "Experimente isto" porque o operador + define pelo menos uma instância de "por":</span><span class="sxs-lookup"><span data-stu-id="8d611-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="8d611-119">Os operadores de repetição seguem regras normais de precedência e se aplicam ao item de texto imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="8d611-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="8d611-120">Por exemplo, a gramática a seguir resulta em "Nova York" e "Nova York York", mas não em "Nova York Nova York":</span><span class="sxs-lookup"><span data-stu-id="8d611-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="8d611-121">Portanto, normalmente você desejará usar esses operadores com os caracteres de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="8d611-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="8d611-122">Por exemplo, a gramática a seguir inclui "Nova York" e "Nova York Nova York":</span><span class="sxs-lookup"><span data-stu-id="8d611-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="8d611-123">Os operadores de repetição são úteis quando você deseja compor uma gramática que inclui uma sequência repetida, como um número de telefone ou uma especificação de uma lista de itens:</span><span class="sxs-lookup"><span data-stu-id="8d611-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="8d611-124">Embora os operadores também possam ser usados com colchetes (um caractere de agrupamento opcional), isso pode reduzir a eficiência do processamento da gramática do agente.</span><span class="sxs-lookup"><span data-stu-id="8d611-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="8d611-125">Você também pode usar reticências (...) para dar suporte à chamada de *palavras*, ou seja, dizer ao mecanismo de reconhecimento de fala para ignorar palavras faladas nessa posição na frase (às vezes chamadas de palavras de *lixo* ).</span><span class="sxs-lookup"><span data-stu-id="8d611-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="8d611-126">Portanto, o mecanismo de fala reconhece apenas palavras específicas na cadeia de caracteres, independentemente de quando falado com palavras ou frases adjacentes.</span><span class="sxs-lookup"><span data-stu-id="8d611-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="8d611-127">Por exemplo, se você definir essa propriedade como " \[ ... \] verificar email \[ ... \] "o mecanismo de reconhecimento de fala corresponderá a frases como" Verifique emails "ou" verificar email "para este comando.</span><span class="sxs-lookup"><span data-stu-id="8d611-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="8d611-128">As reticências podem ser usadas em qualquer lugar dentro de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8d611-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="8d611-129">No entanto, tenha cuidado ao usar essa técnica, pois as configurações de voz com reticências podem aumentar o potencial de correspondências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="8d611-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="8d611-130">Ao definir as palavras e a gramática para o comando, sempre certifique-se de incluir pelo menos uma palavra necessária; ou seja, evite fornecer apenas palavras opcionais.</span><span class="sxs-lookup"><span data-stu-id="8d611-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="8d611-131">Além disso, certifique-se de que a palavra inclua apenas palavras e letras pronunciadas.</span><span class="sxs-lookup"><span data-stu-id="8d611-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="8d611-132">Para números, é melhor soletrar a palavra em vez de usar a representação numérica.</span><span class="sxs-lookup"><span data-stu-id="8d611-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="8d611-133">Além disso, omita qualquer pontuação ou símbolo.</span><span class="sxs-lookup"><span data-stu-id="8d611-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="8d611-134">Por exemplo, em vez de " \# $1 10 pizza!", use "o número de 1 10 dólar pizza".</span><span class="sxs-lookup"><span data-stu-id="8d611-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="8d611-135">Incluir caracteres não pronunciados ou símbolos para um comando pode fazer com que o mecanismo de fala falhe ao compilar a gramática para todos os seus comandos.</span><span class="sxs-lookup"><span data-stu-id="8d611-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="8d611-136">Por fim, torne seu parâmetro de voz tão distinto como razoavelmente possível de outros comandos de voz que você definir.</span><span class="sxs-lookup"><span data-stu-id="8d611-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="8d611-137">Quanto maior a similaridade entre a gramática de voz para comandos, mais provável será que o mecanismo de fala faça um erro de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="8d611-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="8d611-138">Você também pode usar as pontuações de confiança para distinguir melhor entre dois comandos que podem ter uma gramática de voz semelhante ou semelhante a som.</span><span class="sxs-lookup"><span data-stu-id="8d611-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="8d611-139">Definir a propriedade de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) habilita automaticamente os serviços de fala do agente, disponibilizando a chave de escuta e a dica de escuta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8d611-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="8d611-140">No entanto, ele não carrega o mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="8d611-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="8d611-141">Os recursos de gramática disponíveis podem depender do mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="8d611-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="8d611-142">Talvez você queira verificar com o fornecedor do mecanismo para determinar quais opções de gramática têm suporte.</span><span class="sxs-lookup"><span data-stu-id="8d611-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="8d611-143">Use [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) para especificar um mecanismo.</span><span class="sxs-lookup"><span data-stu-id="8d611-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8d611-144">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8d611-144">See Also</span></span>

<span data-ttu-id="8d611-145">[**IAgentCommand:: getvoice**](iagentcommand--getvoice.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setativated**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="8d611-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 