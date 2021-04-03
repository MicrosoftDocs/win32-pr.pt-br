---
title: IAgentCharacterEx getarquivodeajudaname
description: IAgentCharacterEx getarquivodeajudaname
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916473"
---
# <a name="iagentcharacterexgethelpfilename"></a>IAgentCharacterEx:: getarquivodeajudaname

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário clicar no caractere ou selecionar um comando no menu pop-up. Se houver um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 




