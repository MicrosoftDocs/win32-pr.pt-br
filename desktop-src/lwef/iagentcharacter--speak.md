---
title: IAgentCharacter Speak
description: IAgentCharacter Speak
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014206"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter::Speak

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Fala o arquivo de texto ou som.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

O texto que o caractere deve falar.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

A URL (ou especificação de arquivo) de um arquivo de som a ser usado para a saída falada. Pode ser um arquivo de som padrão (. WAV) ou arquivo de som aprimorado linguisticamente (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID [**da**](/windows/desktop/lwef/iagentcharacter--speak) solicitação de Fala.

</dd> </dl>

Para usar esse método com um caractere configurado para falar usando um mecanismo de TTS (texto em fala), basta fornecer o *parâmetro bszText.* Você pode incluir caracteres de barra vertical ( ) no parâmetro bszText para designar cadeias de caracteres alternativas, de modo que cada vez que o servidor processa o método, ele escolha aleatoriamente uma cadeia de \| caracteres diferente.  O suporte à saída TTS é definido quando o caractere é compilado usando o Editor de Caracteres do Microsoft Agent.

Se você quiser usar a saída do arquivo de som para o caractere, especifique o local do arquivo no *parâmetro bszURL.* Ao usar o protocolo HTTP para baixar um arquivo de som, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade do arquivo antes de usar esse método. Você pode usar o *parâmetro bszText* para especificar as palavras que aparecem no balão de palavras do caractere. Se você especificar um arquivo de som linguisticamente aprimorado (. LWV) para o *parâmetro bszURL* e não especificar texto, o *parâmetro bszText* usa o texto armazenado no arquivo.

O [**método Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa a última animação reproduzda para determinar qual animação de fala deve ser reproduzda. Por exemplo, se você preceder o comando **Speak** com [**um IAgentCharacter::P lay**](iagentcharacter--play.md) "**GestureRight**", o servidor reproduzirá **GestureRight** e, em seguida, a animação de fala **GestureRight.** Se a última animação tocada não tiver animação de fala, o Microsoft Agent reproduz a animação atribuída ao estado **De fala do** caractere.

Se você chamar [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) e o canal de áudio estiver ocupado, a saída de áudio do caractere não será escutada, mas o texto será exibido na palavra balão. A propriedade [Enabled](enabled-property.md) da palavra balão também deve ser **True** para que o texto seja exibido.

A quebra automática de palavras do Microsoft Agent no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço e guia). No entanto, ele também pode quebrar uma palavra para se ajustar ao balão. Em idiomas como japonês, chinês e tailandês, em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> De definir a ID de idioma do caractere (usando [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar o método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantir a exibição de texto apropriada dentro do balão de palavras.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::P lay**](iagentcharacter--play.md), [**IAgentBalllay::GetEnabled,**](iagentballoon--getenabled.md) [**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 