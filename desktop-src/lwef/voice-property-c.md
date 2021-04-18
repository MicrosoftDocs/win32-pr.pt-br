---
title: Propriedade Voice (objeto Command)
description: Propriedade de voz
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105794622"
---
# <a name="voice-property-command-object"></a><span data-ttu-id="41592-103">Propriedade Voice (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="41592-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="41592-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41592-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="41592-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="41592-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="41592-106">Retorna ou define o texto que é passado para a gramática do mecanismo de fala (para reconhecimento) para corresponder a esse [**comando**](/windows/desktop/lwef/the-command-object) para o caractere.</span><span class="sxs-lookup"><span data-stu-id="41592-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="41592-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="41592-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="41592-108">\*Agente \***. Caracteres ("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Cadeia de caracteres* de voz\]</span><span class="sxs-lookup"><span data-stu-id="41592-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="41592-109">Parte</span><span class="sxs-lookup"><span data-stu-id="41592-109">Part</span></span>     | <span data-ttu-id="41592-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="41592-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41592-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="41592-111">*string*</span></span> | <span data-ttu-id="41592-112">Uma expressão de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="41592-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41592-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="41592-113">Remarks</span></span>

<span data-ttu-id="41592-114">Se você não fornecer esse parâmetro, o [**VoiceCaption**](voicecaption-property.md) para o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) não aparecerá na janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="41592-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="41592-115">Se você especificar um parâmetro de [**voz**](voice-property.md) , mas não um **VoiceCaption** (ou uma [**legenda**](https://www.bing.com/search?q=**Caption**)), o comando não aparecerá na janela de comandos de voz, mas ele será acessível por voz quando o aplicativo cliente se tornar entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="41592-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="41592-116">Sua expressão de cadeia de caracteres pode incluir caracteres de colchetes ( \[ \] ) para indicar palavras opcionais e caracteres de barra vertical ( \| ) para indicar cadeias alternativas.</span><span class="sxs-lookup"><span data-stu-id="41592-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="41592-117">As alternativas devem ser colocadas entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="41592-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="41592-118">Por exemplo, "(Olá \[ \] \| , Oi Olá)" diz ao mecanismo de fala para aceitar "Olá", "Olá", "ou" Olá "para o comando.</span><span class="sxs-lookup"><span data-stu-id="41592-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="41592-119">Lembre-se de incluir os espaços apropriados entre o texto entre colchetes ou parênteses e o texto que não está entre colchetes ou parênteses.</span><span class="sxs-lookup"><span data-stu-id="41592-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="41592-120">Você pode usar o operador Star ( \* ) para especificar zero ou mais instâncias das palavras incluídas no grupo ou o operador de adição (+) para especificar uma ou mais instâncias.</span><span class="sxs-lookup"><span data-stu-id="41592-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="41592-121">Por exemplo, os seguintes resultados em uma gramática que dá suporte a "Experimente isto", "Tente isso", "Tente isso", com iterações ilimitadas de "favor":</span><span class="sxs-lookup"><span data-stu-id="41592-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="41592-122">O seguinte formato de gramática exclui "Experimente isto" porque o operador + define pelo menos uma instância de "por":</span><span class="sxs-lookup"><span data-stu-id="41592-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="41592-123">Os operadores de repetição seguem regras normais de precedência e se aplicam ao item de texto imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="41592-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="41592-124">Por exemplo, a gramática a seguir resulta em "Nova York" e "Nova York York", mas não em "Nova York Nova York":</span><span class="sxs-lookup"><span data-stu-id="41592-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="41592-125">Portanto, normalmente você deseja usar esses operadores com os caracteres de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="41592-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="41592-126">Por exemplo, a gramática a seguir inclui "Nova York" e "Nova York Nova York":</span><span class="sxs-lookup"><span data-stu-id="41592-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="41592-127">Os operadores de repetição são úteis quando você deseja compor uma gramática que inclua uma sequência repetida, como um número de telefone ou uma especificação de uma lista de itens.</span><span class="sxs-lookup"><span data-stu-id="41592-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="41592-128">Embora os operadores também possam ser usados com o caractere de agrupamento de colchetes opcionais, fazer isso pode reduzir a eficiência do processamento da gramática do agente.</span><span class="sxs-lookup"><span data-stu-id="41592-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="41592-129">Você também pode usar reticências (...) para dar suporte à chamada de *palavras*, ou seja, dizer ao mecanismo de reconhecimento de fala para ignorar palavras faladas nessa posição na frase (às vezes chamadas de palavras de *lixo* ).</span><span class="sxs-lookup"><span data-stu-id="41592-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="41592-130">Portanto, o mecanismo de fala reconhece apenas palavras específicas na cadeia de caracteres, independentemente de quando falado com palavras ou frases adjacentes.</span><span class="sxs-lookup"><span data-stu-id="41592-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="41592-131">Por exemplo, se você definir essa propriedade como " \[ ... \] verificar email \[ ... \] ", o mecanismo de reconhecimento de fala corresponderá a frases como" verificar email "ou" verificar email "para este comando.</span><span class="sxs-lookup"><span data-stu-id="41592-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="41592-132">As reticências podem ser usadas em qualquer lugar dentro de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="41592-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="41592-133">No entanto, tenha cuidado ao usar essa técnica, pois ela pode aumentar o potencial de correspondências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="41592-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="41592-134">Ao definir a palavra-gramática para o comando, inclua pelo menos uma palavra necessária; ou seja, evite fornecer apenas palavras opcionais.</span><span class="sxs-lookup"><span data-stu-id="41592-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="41592-135">Além disso, certifique-se de que a palavra inclua apenas palavras e letras pronunciadas.</span><span class="sxs-lookup"><span data-stu-id="41592-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="41592-136">Para números, é melhor soletrar a palavra em vez de usar uma representação ambígua.</span><span class="sxs-lookup"><span data-stu-id="41592-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="41592-137">Por exemplo, "345" não é um bom formato de gramática.</span><span class="sxs-lookup"><span data-stu-id="41592-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="41592-138">Da mesma forma, em vez de "IEEE", use "I Triple E".</span><span class="sxs-lookup"><span data-stu-id="41592-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="41592-139">Além disso, omita qualquer pontuação ou símbolo.</span><span class="sxs-lookup"><span data-stu-id="41592-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="41592-140">Por exemplo, em vez de " \# $1 10 pizza!", use "o número de 1 10 dólar pizza".</span><span class="sxs-lookup"><span data-stu-id="41592-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="41592-141">Incluir caracteres não pronunciados ou símbolos para um comando pode fazer com que o mecanismo de fala falhe ao compilar a gramática para todos os seus comandos.</span><span class="sxs-lookup"><span data-stu-id="41592-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="41592-142">Por fim, torne seu parâmetro de voz tão distinto como razoavelmente possível de outros comandos de voz que você definir.</span><span class="sxs-lookup"><span data-stu-id="41592-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="41592-143">Quanto maior a similaridade entre a gramática de voz para comandos, mais provável será que o mecanismo de fala faça um erro de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="41592-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="41592-144">Você também pode usar as pontuações de confiança para distinguir melhor entre dois comandos que podem ter uma gramática de voz semelhante ou semelhante a som.</span><span class="sxs-lookup"><span data-stu-id="41592-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="41592-145">Você pode incluir em suas palavras-gramáticas na forma de *" \\ pronúncia de texto*", em que *texto* é o texto exibido e a *pronúncia* é o texto que esclarece a pronúncia.</span><span class="sxs-lookup"><span data-stu-id="41592-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="41592-146">Por exemplo, a gramática, "1º \\ primeiro", seria reconhecida quando o usuário disser "First", mas o evento de [**comando**](/windows/desktop/lwef/the-command-object) retornará o texto "1º \\ primeiro".</span><span class="sxs-lookup"><span data-stu-id="41592-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="41592-147">Você também pode usar IPA (alfabeto fonético internacional) para especificar uma pronúncia, começando a pronúncia com um caractere de sinal de sustenido (" \# ") e, em seguida, inclua o texto que representa a pronúncia IPA.</span><span class="sxs-lookup"><span data-stu-id="41592-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="41592-148">Para mecanismos de reconhecimento de fala em Japonês, você pode definir a gramática na forma "*kana \\ kanji*", reduzindo as pronúncias alternativas e aumentando a precisão.</span><span class="sxs-lookup"><span data-stu-id="41592-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="41592-149">(A ordenação é revertida para compatibilidade com versões anteriores.) Isso é particularmente importante para a pronúncia de nomes próprios em kanji.</span><span class="sxs-lookup"><span data-stu-id="41592-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="41592-150">No entanto, você pode apenas passar kanji sem o kana e, nesse caso, o mecanismo deve escutar todas as pronúncias aceitáveis para o kanji.</span><span class="sxs-lookup"><span data-stu-id="41592-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="41592-151">Você também pode passar apenas kana.</span><span class="sxs-lookup"><span data-stu-id="41592-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="41592-152">Observe também que, para idiomas como japonês, chinês e tailandês, que não usam caracteres de espaço para designar quebras de palavras, insira um caractere de espaço de largura zero (0x200B) Unicode para indicar quebras de palavras lógicas.</span><span class="sxs-lookup"><span data-stu-id="41592-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="41592-153">Exceto por erros que usam os caracteres de formatação de repetição ou agrupamento, o Agent não relatará erros na sua gramática, a menos que o mecanismo em si relate o erro.</span><span class="sxs-lookup"><span data-stu-id="41592-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="41592-154">Se você passar o texto na sua gramática de que o mecanismo não consegue compilar, mas o mecanismo não tratar e retornar como erro, o Agent não poderá relatar o erro.</span><span class="sxs-lookup"><span data-stu-id="41592-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="41592-155">Portanto, o aplicativo cliente deve ser definir cuidadosamente a gramática para a propriedade de [**voz**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="41592-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="41592-156">Os recursos de gramática disponíveis podem depender do mecanismo de reconhecimento de fala.</span><span class="sxs-lookup"><span data-stu-id="41592-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="41592-157">Talvez você queira verificar com o fornecedor do mecanismo para determinar quais opções de gramática têm suporte.</span><span class="sxs-lookup"><span data-stu-id="41592-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="41592-158">Use o [**SRModeID**](srmodeid-property.md) para usar um mecanismo específico.</span><span class="sxs-lookup"><span data-stu-id="41592-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="41592-159">A operação dessa propriedade depende do estado da propriedade de reconhecimento de fala do servidor.</span><span class="sxs-lookup"><span data-stu-id="41592-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="41592-160">Por exemplo, se o reconhecimento de fala estiver desabilitado ou não estiver instalado, essa propriedade não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="41592-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
