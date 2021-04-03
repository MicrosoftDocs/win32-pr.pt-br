---
title: IAgentCharacterEx setarquivodeajudaname
description: IAgentCharacterEx setarquivodeajudaname
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084078"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx:: setarquivodeajudaname

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Define o HelpFilename para um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

O nome de arquivo da ajuda para o caractere.

</dd> </dl>

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário clicar no caractere ou selecionar um comando no menu pop-up. Se houver um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: getarquivodeajudaname**](iagentcharacterex--gethelpfilename.md)


 

 




