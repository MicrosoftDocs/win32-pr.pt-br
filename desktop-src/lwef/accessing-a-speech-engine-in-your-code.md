---
title: Acessando um mecanismo de fala em seu código
description: Acessando um mecanismo de fala em seu código
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105810706"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Acessando um mecanismo de fala em seu código

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para usar um mecanismo de fala específico em seu código, use a API do agente para definir o mecanismo. Para mecanismos de entrada de fala, use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**), ESPECIFICANDO a ID de modo para o mecanismo. No entanto, observe que o mecanismo deve ser instalado. Para determinar se o mecanismo está presente, você pode consultar **SRModeID**. O mecanismo deve corresponder à configuração [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) do caractere. Por exemplo, você não pode definir **SRModeID** como uma ID de modo de mecanismo de reconhecimento de fala em alemão para um caractere cuja **LanguageID** é francês.

**IDs do modo de mecanismo de entrada de fala**



| Voz                                    | IDs de modo                             |
|------------------------------------------|--------------------------------------|
| Mecanismo de reconhecimento de fala da Microsoft v 4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Verifique e defina os [**idiomas**](https://www.bing.com/search?q=**LanguageID**) e [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) do caractere em seu código antes de tentar definir a gramática para os parâmetros de voz dos objetos de **comando** do seu aplicativo. Considere também verificar o navegador ou o idioma do sistema para que você possa ter certeza de que corresponde à configuração de seus usuários. O mecanismo poderá falhar se você tentar definir uma gramática para um idioma para o qual o mecanismo não corresponde.

Um conjunto de caracteres para a saída de conversão de texto em fala (TTS) pode ser compilado com uma preferência de ID de modo do mecanismo de saída de fala padrão. Quando o caractere for carregado, se o mecanismo estiver instalado e corresponder à [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)do caractere, o Agent tentará carregar essa ID de modo para saída de fala. Se o mecanismo não estiver presente ou tiver uma **LanguageID** diferente, o Agent tentará carregar a primeira ID de modo que encontrará que corresponde à **LanguageID** do caractere, mas ainda definirá a velocidade compilada e a configuração de densidade do caractere.

Observe que, como todos os caracteres fornecidos pelo agente da Microsoft são compilados para usar o Lernout & Hauspie TruVoice American English Engine como o mecanismo de saída de fala padrão, a configuração de velocidade e densidade dos caracteres é ajustada para esse idioma e mecanismo. Portanto, ao usar outros mecanismos de TTS ou mecanismos de outras linguagens, os caracteres não podem falar na densidade ou velocidade ideal. Embora seu aplicativo ou página da Web não possa gravar os valores de propriedade de [**densidade**](/previous-versions/ms809428(v=msdn.10)) e [**velocidade**](https://www.bing.com/search?q=**Speed**) , você pode incluir marcas [Pit](pit-tag.md) (Pitch) e [SPD](spd-tag.md) (Speed) no texto de saída que alterarão temporariamente a densidade e a velocidade de um determinado expressão. No entanto, usar as marcas Pit e SPD não alterará as propriedades de **densidade** e **velocidade** . Consulte [programação do controle do Microsoft Agent](programming-the-microsoft-agent-control.md) e as [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md) para obter detalhes.

Você também precisa instalar os binários de tempo de execução do SAPI 4.0 (SPCHAPI.exe) ao usar outros mecanismos de TTS compatíveis com SAPI que o mecanismo de inglês do L&H TruVoice American em inglês com os caracteres fornecidos pelo agente da Microsoft para que os mecanismos sejam enumerados corretamente. Na página da Web, inclua a seguinte marca de objeto para instalar automaticamente o componente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Para consultar ou definir a ID de modo de um mecanismo, use [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Com **TTSModeID** , você pode definir uma ID de modo diferente da [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)do caractere. Por exemplo, você pode definir um caractere alemão para falar usando uma ID de modo francês. As IDs do modo de mecanismo de saída de fala não só definem qual mecanismo você usa, mas também correspondem a vozes específicas com suporte para um mecanismo. Você também pode usar o editor de caracteres do Microsoft Agent ou as ferramentas incluídas na [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx) para consultar as IDs de modo dos mecanismos de TTS instalados no sistema.

**IDs do modo de saída de fala**



| Voz                                       | IDs de modo                               |
|---------------------------------------------|----------------------------------------|
| Adulto fêmea \# 1, inglês americano, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adulto fêmea \# 2, inglês americano, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adulto macho \# 1, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adulto macho \# 2, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adulto macho \# 3, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adulto macho \# 4, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adulto macho \# 5, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adulto macho \# 6, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adulto macho \# 7, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adulto macho \# 8, inglês americano, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, inglês britânico, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, inglês britânico, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda, holandês, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, holandês, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, francês, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Pierre, francês, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, alemão, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, alemão, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Bárbara, italiano, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano, italiano, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko, japonês, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, japonês, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-Ah, coreano, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Jun-Ho, coreano, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Juliana, Português (Brasil), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre, Português (Brasil), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, russo, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris, russo, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen, espanhol, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, espanhol, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Há uma diferença entre o CLSID de instalação do mecanismo de fala e sua ID de modo. Da mesma forma, um mecanismo de fala também tem uma ID de mecanismo, mas essa ID não é aplicável na API do agente.

 

 

 