---
title: Método Speak
description: Método Speak
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475338"
---
# <a name="speak-method"></a>Método Speak

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Fala o arquivo de texto ou som especificado para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Fale_ *  \[ *texto,* \] \[ *URL*\]



| Parte   | Descrição                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | Opcional. Uma cadeia de caracteres que especifica o que o caractere diz.                                                                                                                                                                                                   |
| *URL*  | Opcional. Uma expressão de cadeia de caracteres que especifica o local de um arquivo de áudio (. WAV ou . Formato LWV). O local pode ser especificado como um arquivo (incluindo uma especificação de caminho UNC) ou URL (quando os dados de animação de caracteres também estão sendo recuperados por meio do protocolo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Embora os *parâmetros* Text e *Url* sejam opcionais, um deles deve ser fornecido. Para usar esse método com um caractere configurado para falar apenas em seu balão de palavra ou usando um mecanismo de TTS (texto em fala), basta fornecer o *parâmetro* Text. Inclua um espaço entre palavras para definir quebras de palavras apropriadas no balão de palavras, mesmo para idiomas que tradicionalmente não incluem espaços.

Você também pode incluir caracteres de barra vertical ( ) no parâmetro Text para designar cadeias de caracteres alternativas, para que o servidor escolha aleatoriamente uma cadeia de caracteres diferente sempre que ele \| processa o  método.

O suporte a caracteres da saída TTS é definido quando o caractere é compilado usando o Editor de Caracteres do Microsoft Agent. Para gerar a saída do TTS, um mecanismo TTS compatível já deve estar instalado antes de chamar esse método. Para obter mais informações, consulte [Acessando os Serviços de Fala.](accessing-speech-services.md)

Se você usar o arquivo de som gravado (. WAV ou . Saída somente de formato LWV) para o caractere, especifique o local do arquivo no parâmetro *URL.* Essa especificação de arquivo pode incluir um caminho local (absoluto ou relativo) ou UNC (convenção de nomenização universal). O nome do arquivo não pode incluir caracteres não incluídos na página de código dos EUA 1252. No entanto, se você estiver usando o protocolo HTTP para acessar os dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação antes de chamar o **método Speak.** Consulte [Usando a Ferramenta de Edição de Som de Informações Linguísticas da Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obter informações sobre o criativo. Arquivos LWV.

Ao usar a saída de arquivo de som gravada, você ainda pode usar o parâmetro *Text* para especificar as palavras que aparecem no balão de palavras do caractere. No entanto, se você especificar um arquivo de som linguisticamente aprimorado (. LWV) para o parâmetro *URL* e não especificar texto para a palavra balão, o parâmetro *Text* usa o texto armazenado no arquivo.

Você também pode variar os parâmetros da saída de fala com marcas especiais que você inclui no *parâmetro* Text. Para obter mais informações, consulte [Marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Você pode usar isso para sincronizar outras partes do código com a saída falada do caractere, como no exemplo a seguir:


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



Você também pode usar um [**objeto Request**](/windows/desktop/lwef/the-request-object) para verificar se há determinadas condições de erro. Por exemplo, se você usar o método **Speak** para falar e não tiver  um mecanismo TTS compatível instalado, o servidor define a propriedade [**Status**](status-property.md) do objeto Request como "failed" com sua propriedade [**Description**](description-property.md) como "Class not registered" ou "Unknown or object returned error". Para determinar se você tem um mecanismo TTS instalado, use a [**propriedade TTSModeID.**](ttsmodeid-property.md)

Da mesma forma, se você tiver a tentativa de caractere de falar um arquivo de som e se o [](/windows/desktop/lwef/the-request-object) arquivo não tiver sido carregado ou houver um problema com o dispositivo de áudio, o servidor também define a propriedade [**Status**](status-property.md) do objeto request como "failed" com um número de código de erro apropriado.

Você também pode incluir marcas de fala de indicador no texto Falar para sincronizar seu código:


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



Para obter mais informações sobre a marca de fala do indicador, consulte [Marcas de Saída de Fala](mrk-tag.md).

O **método Speak** usa a última ação tocada para determinar qual animação de fala deve ser reproduzda. Por exemplo, se você precedeu o comando **Speak** com um [**Play**](play-method.md) "**GestureRight**", o servidor reproduzirá **GestureRight** e, em seguida, a animação **de fala GestureRight.** Se a última animação tocada não tiver animação de fala, o Agent reproduz a animação atribuída ao estado De **fala do** caractere.

Se você chamar **Speak** e o canal de áudio estiver ocupado, a saída de áudio do caractere não será escutada, mas o texto será exibido na palavra balão.

A quebra automática de palavras do agente na palavra balão quebra palavras usando caracteres de espaço em branco (por exemplo, Espaço ou Guia). No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão. Em idiomas como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> A propriedade [**Enabled**](enabled-property.md) da palavra balão também deve ser **True para** que o texto seja exibido.

 

> [!Note]  
> De definir a ID de idioma do caractere (definindo **LanguageID** do caractere antes de usar o método **Speak** para garantir a exibição de texto apropriada dentro do balão de palavras.

 

## <a name="see-also"></a>Consulte Também

[**Evento de indicador**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)


 

 