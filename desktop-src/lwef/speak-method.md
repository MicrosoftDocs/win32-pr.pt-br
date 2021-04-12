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
# <a name="speak-method"></a>Método Speak

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Fala o texto ou o arquivo de som especificado para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  \[ *Texto* \] de fala, \[ *URL*\]



| Parte   | Descrição                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | Opcional. Uma cadeia de caracteres que especifica o que diz o caractere.                                                                                                                                                                                                   |
| *URL*  | Opcional. Uma expressão de cadeia de caracteres que especifica o local de um arquivo de áudio (. WAV ou. Formato LWV). O local pode ser especificado como um arquivo (incluindo uma especificação de caminho UNC) ou URL (quando os dados de animação de caracteres também estão sendo recuperados via protocolo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Embora os parâmetros de *texto* e *URL* sejam opcionais, um deles deve ser fornecido. Para usar esse método com um caractere configurado para falar apenas em seu balão de palavra ou usando um mecanismo de conversão de texto em fala (TTS), basta fornecer o parâmetro de *texto* . Inclua um espaço entre as palavras para definir as quebras de palavras apropriadas na palavra balão, mesmo para idiomas que não incluam tradicionalmente espaços.

Você também pode incluir caracteres de barra vertical ( \| ) no parâmetro de *texto* para designar cadeias alternativas, de forma que o servidor escolha aleatoriamente uma cadeia de caracteres diferente sempre que processar o método.

O suporte a caracteres de saída TTS é definido quando o caractere é compilado usando o editor de caracteres do Microsoft Agent. Para gerar a saída de TTS, um mecanismo de TTS compatível já deve estar instalado antes de chamar esse método. Para obter mais informações, consulte [acessando serviços de fala](accessing-speech-services.md).

Se você usar arquivo de som gravado (. WAV ou. Somente formato LWV) para o caractere, especifique o local do arquivo no parâmetro *URL* . Essa especificação de arquivo pode incluir um caminho local (absoluto ou relativo) ou UNC (Convenção de nomenclatura universal). O nome do arquivo não pode incluir nenhum caractere não incluído na página de código 1252 do US. No entanto, se você estiver usando o protocolo HTTP para acessar os dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar a animação antes de chamar o método **Speak** . Consulte [usando a ferramenta de edição de som de informações linguísticas da Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obter informações sobre o Creative. Arquivos LWV.

Ao usar a saída de arquivo de som gravada, você ainda pode usar o parâmetro *Text* para especificar as palavras que aparecem no balão de palavras do caractere. No entanto, se você especificar um arquivo de som com uma melhoria linguística (. LWV) para o parâmetro de *URL* e não especificam texto para o balão de palavras, o parâmetro de *texto* usa o texto armazenado no arquivo.

Você também pode variar os parâmetros da saída de fala com marcas especiais que você inclui no parâmetro *Text* . Para obter mais informações, consulte [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Você pode usar isso para sincronizar outras partes do seu código com a saída falada do caractere, como no exemplo a seguir:


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



Você também pode usar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para verificar determinadas condições de erro. Por exemplo, se você usar o método **Speak** para falar e não tiver um mecanismo de TTS compatível instalado, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com sua propriedade [**Description**](description-property.md) como "Class não registered" ou "Unknown ou Object retornado Error". Para determinar se você tem um mecanismo de TTS instalado, use a propriedade [**TTSModeID**](ttsmodeid-property.md) .

Da mesma forma, se você tiver a tentativa de caractere de falar um arquivo de som e se o arquivo não tiver sido carregado ou houver um problema com o dispositivo de áudio, o servidor também definirá a propriedade [**status**](status-property.md) do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) como "failed" com um número de código de erro apropriado.

Você também pode incluir marcas de fala de indicador no texto de fala para sincronizar seu código:


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



Para obter mais informações sobre a marca de fala de indicador, consulte [marcas de saída de fala](mrk-tag.md).

O método **Speak** usa a última ação executada para determinar qual animação de fala deve ser reproduzida. Por exemplo, se você preceder o comando **Speak** com uma [**reprodução**](play-method.md) "**GestureRight**", o servidor executará **GestureRight** e, em seguida, a animação de **GestureRight** falando. Se a última animação executada não tiver animação de fala, o Agent reproduzirá a animação atribuída ao estado de **fala** do caractere.

Se você ligar para **falar** e o canal de áudio estiver ocupado, a saída de áudio do caractere não será ouvida, mas o texto será exibido na palavra balão.

A quebra automática de palavras do agente no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço ou tabulação). No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão. Em linguagens como japonês, chinês e tailandês, em que os espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> A propriedade [**Enabled**](enabled-property.md) do balão do Word também deve ser **true** para que o texto seja exibido.

 

> [!Note]  
> Defina a ID de idioma do caractere (definindo a **LanguageID** do caractere antes de usar o método **Speak** para garantir a exibição de texto apropriada dentro do balão de palavras.

 

## <a name="see-also"></a>Consulte Também

Evento [**Bookmark**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)


 

 