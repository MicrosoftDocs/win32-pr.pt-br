---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119001"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Define a ID de idioma definida para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

A configuração de ID de idioma para o caractere.

</dd> </dl>

Um inteiro Longo que especifica a ID de idioma do caractere. A LANGID (ID de idioma) de um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário. Você pode usar os valores a seguir para os idiomas especificados. Para obter mais informações, consulte a documentação do SDK da plataforma.



| Idioma              | ID     |  Idioma             | ID     |
|-----------------------|--------|-----------------------|--------|
| Árabe (Árabe)        | 0x0401 | Italiano               | 0x0410 |
| Basco                | 0x042d | Japonês              | 0x0411 |
| Chinês (Simplificado)  | 0x0804 | Coreano                | 0x0412 |
| Chinês (Tradicional) | 0x0404 | Norueguês             | 0x0414 |
| Croata              | 0x041A | Polonês                | 0x0415 |
| Tcheco                 | 0x0405 | Português (Portugal) | 0x0816 |
| Dinamarquês                | 0x0406 | Português (Brasil)   | 0x0416 |
| Holandês                 | 0x0413 | Romeno              | 0x0418 |
| Inglês (britânico)     | 0x0809 | Russo               | 0x0419 |
| Inglês (EUA)          | 0x0409 | Eslovaco             | 0x041B |
| Finlandês               | 0x040B | Esloveno             | 0x0424 |
| Francês                | 0x040C | Espanhol               | 0x0C0A |
| Alemão                | 0x0407 | Sueco               | 0x041D |
| Grego                 | 0x0408 | Tailandês                  | 0x041e |
| Hebraico                | 0x040D | Turco               | 0x041F |
| Húngaro             | 0x040E |                       |        |



 

Se você não definir a ID de idioma para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL de idioma do Agent correspondente estiver instalada; caso contrário, o idioma do caractere será Inglês (EUA).

Essa propriedade também determina o idioma da palavra texto de balão, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala. Ele também determina o idioma padrão para a saída do TTS. Para determinar se há um mecanismo de fala compatível disponível para a linguagem do caractere, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Se você tentar definir a ID de idioma para um caractere e os recursos de linguagem do Agent, a página de código ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent retornará um erro e a ID do idioma do caractere permanecerá em sua última configuração. Definir essa propriedade não retornará um erro se não houver mecanismos de fala correspondentes para o idioma.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> Se você definir a ID de idioma do caractere para um idioma que dá suporte a texto bidirecional (como árabe ou hebraico), mas o sistema que executa seu aplicativo não tiver suporte bidirecional instalado, o texto aparecerá na palavra balão em ordem lógica em vez de exibir.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




