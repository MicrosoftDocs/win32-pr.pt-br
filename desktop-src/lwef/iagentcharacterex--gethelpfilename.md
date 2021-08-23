---
title: IAgentCharacterEx getarquivodeajudaname
description: IAgentCharacterEx getarquivodeajudaname
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba5acdcfef90d1918f5c4697127b4449e96f2667b20a2de0230fcdf2cd6dd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105524"
---
# <a name="iagentcharacterexgethelpfilename"></a>IAgentCharacterEx:: getarquivodeajudaname

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

Recupera o HelpFilename de um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Endereço de uma variável que recebe o nome de arquivo da ajuda para o caractere.

</dd> </dl>

se você tiver criado um arquivo de ajuda Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent automaticamente chamará Help quando [**HelpModeOn**](helpmodeon-property.md) for definido como **True** e o usuário clicar no caractere ou selecionar um comando no menu pop-up. Se houver um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> a criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 




