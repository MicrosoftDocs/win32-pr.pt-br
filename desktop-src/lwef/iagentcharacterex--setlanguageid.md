---
title: IAgentCharacterEx setlanguageid
description: IAgentCharacterEx setlanguageid
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635361"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx:: setlanguageid

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Define o ID de idioma definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

A configuração de ID de idioma para o caractere.

</dd> </dl>

Um inteiro longo que especifica a ID de idioma para o caractere. A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário. Você pode usar os seguintes valores para os idiomas especificados. Para obter mais informações, consulte a documentação do Platform SDK.



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| Árabe (Arábia)        | 0x0401 | Italiano               | 0x0410 |
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
| Grego                 | 0x0408 | Tailandês                  | 0x041E |
| Hebraico                | 0x040D | Turco               | 0x041F |
| Húngaro             | 0x040E |                       |        |



 

Se você não definir a ID de idioma para o caractere, sua ID de idioma será a ID de idioma do sistema atual se a DLL do idioma do agente correspondente estiver instalada; caso contrário, o idioma do caractere será inglês (EUA).

Essa propriedade também determina o idioma do texto do balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala. Ele também determina o idioma padrão para a saída de TTS. Para determinar se há um mecanismo de fala compatível disponível para o idioma do caractere, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Se você tentar definir a ID de idioma para um caractere e os recursos de idioma do agente, a página de código ou uma fonte de exibição para a ID do idioma não estiver disponível, o Agent retornará um erro e a ID do idioma do caractere permanecerá em sua última configuração. Definir essa propriedade não retornará um erro se não houver nenhum mecanismo de fala correspondente para o idioma.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> Se você definir a ID de idioma do caractere como um idioma que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema que executa o aplicativo não tem suporte bidirecional instalado, o texto aparecerá no balão de palavras em lógica em vez de em ordem de exibição.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx: Getlanguageid**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




