---
title: IAgentCharacter falar
description: IAgentCharacter falar
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499038"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="d5619-103">IAgentCharacter:: falar</span><span class="sxs-lookup"><span data-stu-id="d5619-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="d5619-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5619-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="d5619-105">Fala o arquivo de texto ou de som.</span><span class="sxs-lookup"><span data-stu-id="d5619-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="d5619-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5619-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d5619-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="d5619-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="d5619-108">O texto que o caractere deve falar.</span><span class="sxs-lookup"><span data-stu-id="d5619-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="d5619-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span><span class="sxs-lookup"><span data-stu-id="d5619-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="d5619-110">A URL (ou a especificação de arquivo) de um arquivo de som a ser usado para a saída falada.</span><span class="sxs-lookup"><span data-stu-id="d5619-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="d5619-111">Esse pode ser um arquivo de som padrão (. WAV) ou um arquivo de som aprimorado linguística (. LWV).</span><span class="sxs-lookup"><span data-stu-id="d5619-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="d5619-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="d5619-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d5619-113">Endereço de uma variável que recebe a ID da solicitação de [**fala**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="d5619-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d5619-114">Para usar esse método com um caractere configurado para falar usando um mecanismo de conversão de texto em fala (TTS); Basta fornecer o parâmetro *bszText* .</span><span class="sxs-lookup"><span data-stu-id="d5619-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="d5619-115">Você pode incluir caracteres de barra vertical ( \| ) no parâmetro *bszText* para designar cadeias alternativas, para que cada vez que o servidor processe o método, ele escolha aleatoriamente uma cadeia de caracteres diferente.</span><span class="sxs-lookup"><span data-stu-id="d5619-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="d5619-116">O suporte à saída de TTS é definido quando o caractere é compilado usando o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d5619-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d5619-117">Se você quiser usar a saída do arquivo de som para o caractere, especifique o local para o arquivo no parâmetro *bszURL* .</span><span class="sxs-lookup"><span data-stu-id="d5619-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="d5619-118">Ao usar o protocolo HTTP para baixar um arquivo de som, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade do arquivo antes de usar esse método.</span><span class="sxs-lookup"><span data-stu-id="d5619-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="d5619-119">Você pode usar o parâmetro *bszText* para especificar as palavras que aparecem no balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="d5619-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="d5619-120">Se você especificar um arquivo de som com uma melhoria linguística (. LWV) para o parâmetro *bszURL* e não especifica texto, o parâmetro *bszText* usa o texto armazenado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="d5619-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="d5619-121">O método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa a última animação executada para determinar qual animação de fala deve ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="d5619-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="d5619-122">Por exemplo, se você preceder o comando **Speak** com um [**IAgentCharacter::P deite**](iagentcharacter--play.md) "**GestureRight**", o servidor tocará **GestureRight** e, em seguida, a animação de língua **GestureRight** .</span><span class="sxs-lookup"><span data-stu-id="d5619-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="d5619-123">Se a última animação não tiver animação de fala, o Microsoft Agent reproduzirá a animação atribuída ao estado de **fala** do caractere.</span><span class="sxs-lookup"><span data-stu-id="d5619-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="d5619-124">Se você ligar para [**falar**](/windows/desktop/lwef/iagentcharacter--speak) e o canal de áudio estiver ocupado, a saída de áudio do caractere não será ouvida, mas o texto será exibido na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="d5619-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="d5619-125">A propriedade [Enabled](enabled-property.md) do balão do Word também deve ser **verdadeira** para o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="d5619-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="d5619-126">A quebra automática de palavras do Microsoft Agent na palavra balão, quebra palavras usando caracteres de espaço em branco (por exemplo, espaço e tabulação).</span><span class="sxs-lookup"><span data-stu-id="d5619-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="d5619-127">No entanto, ele pode quebrar uma palavra para se ajustar também ao balão.</span><span class="sxs-lookup"><span data-stu-id="d5619-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="d5619-128">Em linguagens como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.</span><span class="sxs-lookup"><span data-stu-id="d5619-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="d5619-129">Defina a ID de idioma do caractere (usando [**IAgentCharacterEx:: Setlanguageid**](iagentcharacterex--setlanguageid.md) antes de usar o método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantir a exibição de texto apropriada dentro do balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="d5619-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d5619-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d5619-130">See Also</span></span>

<span data-ttu-id="d5619-131">[**IAgentCharacter::P deite**](iagentcharacter--play.md), [**IAgentBalloon:: gethabilited**](iagentballoon--getenabled.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md)</span><span class="sxs-lookup"><span data-stu-id="d5619-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 