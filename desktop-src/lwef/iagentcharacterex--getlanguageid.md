---
title: IAgentCharacterEx getlanguageid
description: IAgentCharacterEx getlanguageid
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005875"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx:: getlanguageid

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Recupera o conjunto de ID de idioma para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Endereço de uma variável que recebe a configuração de ID de idioma para o caractere.

</dd> </dl>

Um inteiro longo que especifica a ID de idioma para o caractere. A ID de idioma (LANGid) para um caractere é um valor de 16 bits definido pelo Windows, que consiste em uma ID de idioma primário e uma ID de idioma secundário. Os exemplos a seguir são valores para alguns idiomas. Para determinar os valores de outros idiomas, consulte a documentação do Platform SDK.



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



 

Se você não definir essa ID de idioma para o caractere, a ID de idioma do caractere será a ID do idioma atual do sistema.

Essa configuração também determina o idioma da saída TTS, o texto do balão do Word, os comandos no menu pop-up do caractere e o mecanismo de reconhecimento de fala. Para determinar se há um mecanismo de reconhecimento de fala compatível disponível para o idioma do caractere, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) ou [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> Se a ID do idioma for definida como um idioma que dá suporte a texto bidirecional (como árabe ou Hebraico), mas o sistema que executa o aplicativo não tiver suporte bidirecional instalado, o texto aparecerá no balão do Word em ordem lógica, em vez de exibição.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx: Setlanguageid**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




