---
title: Método Speak
description: Método Speak
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454016"
---
# <a name="speak-method"></a><span data-ttu-id="1d80c-103">Método Speak</span><span class="sxs-lookup"><span data-stu-id="1d80c-103">Speak Method</span></span>

<span data-ttu-id="1d80c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d80c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1d80c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="1d80c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1d80c-106">Fala o texto ou o arquivo de som especificado para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="1d80c-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="1d80c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="1d80c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1d80c-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  \[ *Texto* \] de fala, \[ *URL*\]</span><span class="sxs-lookup"><span data-stu-id="1d80c-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="1d80c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1d80c-109">Part</span></span>   | <span data-ttu-id="1d80c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d80c-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d80c-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="1d80c-111">*Text*</span></span> | <span data-ttu-id="1d80c-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1d80c-112">Optional.</span></span> <span data-ttu-id="1d80c-113">Uma cadeia de caracteres que especifica o que diz o caractere.</span><span class="sxs-lookup"><span data-stu-id="1d80c-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="1d80c-114">*URL*</span><span class="sxs-lookup"><span data-stu-id="1d80c-114">*Url*</span></span>  | <span data-ttu-id="1d80c-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1d80c-115">Optional.</span></span> <span data-ttu-id="1d80c-116">Uma expressão de cadeia de caracteres que especifica o local de um arquivo de áudio (. WAV ou. Formato LWV).</span><span class="sxs-lookup"><span data-stu-id="1d80c-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="1d80c-117">O local pode ser especificado como um arquivo (incluindo uma especificação de caminho UNC) ou URL (quando os dados de animação de caracteres também estão sendo recuperados via protocolo HTTP).</span><span class="sxs-lookup"><span data-stu-id="1d80c-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d80c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d80c-118">Remarks</span></span>

<span data-ttu-id="1d80c-119">Embora os parâmetros de *texto* e *URL* sejam opcionais, um deles deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="1d80c-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="1d80c-120">Para usar esse método com um caractere configurado para falar apenas em seu balão de palavra ou usando um mecanismo de conversão de texto em fala (TTS), basta fornecer o parâmetro de *texto* .</span><span class="sxs-lookup"><span data-stu-id="1d80c-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="1d80c-121">Inclua um espaço entre as palavras para definir as quebras de palavras apropriadas na palavra balão, mesmo para idiomas que não incluam tradicionalmente espaços.</span><span class="sxs-lookup"><span data-stu-id="1d80c-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="1d80c-122">Você também pode incluir caracteres de barra vertical ( \| ) no parâmetro de *texto* para designar cadeias alternativas, de forma que o servidor escolha aleatoriamente uma cadeia de caracteres diferente sempre que processar o método.</span><span class="sxs-lookup"><span data-stu-id="1d80c-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="1d80c-123">O suporte a caracteres de saída TTS é definido quando o caractere é compilado usando o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1d80c-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1d80c-124">Para gerar a saída de TTS, um mecanismo de TTS compatível já deve estar instalado antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="1d80c-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="1d80c-125">Para obter mais informações, consulte [acessando serviços de fala](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="1d80c-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="1d80c-126">Se você usar arquivo de som gravado (. WAV ou. Somente formato LWV) para o caractere, especifique o local do arquivo no parâmetro *URL* .</span><span class="sxs-lookup"><span data-stu-id="1d80c-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="1d80c-127">Essa especificação de arquivo pode incluir um caminho local (absoluto ou relativo) ou UNC (Convenção de nomenclatura universal).</span><span class="sxs-lookup"><span data-stu-id="1d80c-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="1d80c-128">O nome do arquivo não pode incluir nenhum caractere não incluído na página de código 1252 do US.</span><span class="sxs-lookup"><span data-stu-id="1d80c-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="1d80c-129">No entanto, se você estiver usando o protocolo HTTP para acessar os dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação antes de chamar o método **Speak** .</span><span class="sxs-lookup"><span data-stu-id="1d80c-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="1d80c-130">Consulte [usando a ferramenta de edição de som de informações linguísticas da Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obter informações sobre o Creative. Arquivos LWV.</span><span class="sxs-lookup"><span data-stu-id="1d80c-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="1d80c-131">Ao usar a saída de arquivo de som gravada, você ainda pode usar o parâmetro *Text* para especificar as palavras que aparecem no balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="1d80c-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="1d80c-132">No entanto, se você especificar um arquivo de som com uma melhoria linguística (. LWV) para o parâmetro de *URL* e não especificam texto para o balão de palavras, o parâmetro de *texto* usa o texto armazenado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d80c-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="1d80c-133">Você também pode variar os parâmetros da saída de fala com marcas especiais que você inclui no parâmetro *Text* .</span><span class="sxs-lookup"><span data-stu-id="1d80c-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="1d80c-134">Para obter mais informações, consulte [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="1d80c-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="1d80c-135">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="1d80c-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="1d80c-136">Você pode usar isso para sincronizar outras partes do seu código com a saída falada do caractere, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="1d80c-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="1d80c-137">Você também pode usar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para verificar determinadas condições de erro.</span><span class="sxs-lookup"><span data-stu-id="1d80c-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="1d80c-138">Por exemplo, se você usar o método **Speak** para falar e não tiver um mecanismo de TTS compatível instalado, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com sua propriedade [**Description**](description-property.md) como "Class não registered" ou "Unknown ou Object retornado Error".</span><span class="sxs-lookup"><span data-stu-id="1d80c-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="1d80c-139">Para determinar se você tem um mecanismo de TTS instalado, use a propriedade [**TTSModeID**](ttsmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1d80c-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="1d80c-140">Da mesma forma, se você tiver a tentativa de caractere de falar um arquivo de som e se o arquivo não tiver sido carregado ou houver um problema com o dispositivo de áudio, o servidor também definirá a propriedade [**status**](status-property.md) do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) como "failed" com um número de código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="1d80c-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="1d80c-141">Você também pode incluir marcas de fala de indicador no texto de fala para sincronizar seu código:</span><span class="sxs-lookup"><span data-stu-id="1d80c-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="1d80c-142">Para obter mais informações sobre a marca de fala de indicador, consulte [marcas de saída de fala](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="1d80c-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="1d80c-143">O método **Speak** usa a última ação executada para determinar qual animação de fala deve ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="1d80c-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="1d80c-144">Por exemplo, se você preceder o comando **Speak** com uma [**reprodução**](play-method.md) "**GestureRight**", o servidor executará **GestureRight** e, em seguida, a animação de **GestureRight** falando.</span><span class="sxs-lookup"><span data-stu-id="1d80c-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="1d80c-145">Se a última animação executada não tiver animação de fala, o Agent reproduzirá a animação atribuída ao estado de **fala** do caractere.</span><span class="sxs-lookup"><span data-stu-id="1d80c-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="1d80c-146">Se você ligar para **falar** e o canal de áudio estiver ocupado, a saída de áudio do caractere não será ouvida, mas o texto será exibido na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="1d80c-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="1d80c-147">A quebra automática de palavras do agente no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço ou tabulação).</span><span class="sxs-lookup"><span data-stu-id="1d80c-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="1d80c-148">No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão.</span><span class="sxs-lookup"><span data-stu-id="1d80c-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="1d80c-149">Em linguagens como japonês, chinês e tailandês, em que os espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.</span><span class="sxs-lookup"><span data-stu-id="1d80c-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="1d80c-150">A propriedade [**Enabled**](enabled-property.md) do balão do Word também deve ser **true** para que o texto seja exibido.</span><span class="sxs-lookup"><span data-stu-id="1d80c-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d80c-151">Defina a ID de idioma do caractere (definindo a **LanguageID** do caractere antes de usar o método **Speak** para garantir a exibição de texto apropriada dentro do balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="1d80c-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1d80c-152">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1d80c-152">See Also</span></span>

<span data-ttu-id="1d80c-153">Evento [**Bookmark**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="1d80c-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 