---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9852e5909410f7e51789dd92419af4ef12f11ab0ae7ad0729a26b96a06fe34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477944"
---
# <a name="iagentcharacterexsethelpfilename"></a>IAgentCharacterEx::SetHelpFileName

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

Define o HelpFileName para um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

O nome do arquivo de Ajuda para o caractere.

</dd> </dl>

Se você tiver criado um arquivo de Ajuda do Windows para seu aplicativo e definido a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário clicar no caractere ou selecionar um comando no menu pop-up. Se houver um número de contexto na propriedade [**HelpContextID**](helpcontextid-property.md) do comando selecionado, a Ajuda exibirá um tópico correspondente ao contexto da Ajuda atual; caso contrário, ele exibirá "Nenhum tópico de Ajuda associado a este item".

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)


 

 




