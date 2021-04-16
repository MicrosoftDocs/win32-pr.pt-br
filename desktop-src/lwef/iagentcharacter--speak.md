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
# <a name="iagentcharacterspeak"></a>IAgentCharacter:: falar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Fala o arquivo de texto ou de som.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

O texto que o caractere deve falar.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

A URL (ou a especificação de arquivo) de um arquivo de som a ser usado para a saída falada. Esse pode ser um arquivo de som padrão (. WAV) ou um arquivo de som aprimorado linguística (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de [**fala**](/windows/desktop/lwef/iagentcharacter--speak) .

</dd> </dl>

Para usar esse método com um caractere configurado para falar usando um mecanismo de conversão de texto em fala (TTS); Basta fornecer o parâmetro *bszText* . Você pode incluir caracteres de barra vertical ( \| ) no parâmetro *bszText* para designar cadeias alternativas, para que cada vez que o servidor processe o método, ele escolha aleatoriamente uma cadeia de caracteres diferente. O suporte à saída de TTS é definido quando o caractere é compilado usando o editor de caracteres do Microsoft Agent.

Se você quiser usar a saída do arquivo de som para o caractere, especifique o local para o arquivo no parâmetro *bszURL* . Ao usar o protocolo HTTP para baixar um arquivo de som, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade do arquivo antes de usar esse método. Você pode usar o parâmetro *bszText* para especificar as palavras que aparecem no balão de palavras do caractere. Se você especificar um arquivo de som com uma melhoria linguística (. LWV) para o parâmetro *bszURL* e não especifica texto, o parâmetro *bszText* usa o texto armazenado no arquivo.

O método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa a última animação executada para determinar qual animação de fala deve ser reproduzida. Por exemplo, se você preceder o comando **Speak** com um [**IAgentCharacter::P deite**](iagentcharacter--play.md) "**GestureRight**", o servidor tocará **GestureRight** e, em seguida, a animação de língua **GestureRight** . Se a última animação não tiver animação de fala, o Microsoft Agent reproduzirá a animação atribuída ao estado de **fala** do caractere.

Se você ligar para [**falar**](/windows/desktop/lwef/iagentcharacter--speak) e o canal de áudio estiver ocupado, a saída de áudio do caractere não será ouvida, mas o texto será exibido na palavra balão. A propriedade [Enabled](enabled-property.md) do balão do Word também deve ser **verdadeira** para o texto a ser exibido.

A quebra automática de palavras do Microsoft Agent na palavra balão, quebra palavras usando caracteres de espaço em branco (por exemplo, espaço e tabulação). No entanto, ele pode quebrar uma palavra para se ajustar também ao balão. Em linguagens como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> Defina a ID de idioma do caractere (usando [**IAgentCharacterEx:: Setlanguageid**](iagentcharacterex--setlanguageid.md) antes de usar o método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantir a exibição de texto apropriada dentro do balão de palavras.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::P deite**](iagentcharacter--play.md), [**IAgentBalloon:: gethabilited**](iagentballoon--getenabled.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md)


 

 