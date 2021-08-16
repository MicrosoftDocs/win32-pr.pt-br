---
description: Use as diretrizes a seguir para Windows instalação do Windows que exibe uma caixa de mensagem solicitando que o usuário insira um disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Como autorar mensagens de prompt de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a27b324600b7098c4b11dd94528ce0f3aa624e6859df8d02ef43ee90d632068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381371"
---
# <a name="authoring-disk-prompt-messages"></a>Como autorar mensagens de prompt de disco

Use as diretrizes a seguir para Windows instalação do Windows que exibe uma caixa de mensagem solicitando que o usuário insira um disco.

**Para exibir uma caixa de mensagem solicitando que o usuário insira um disco**

1.  Use os recursos de autor do instalador para definir a cadeia de caracteres de propriedade [**DiskPrompt**](diskprompt.md) na [tabela Propriedade.](property-table.md) Isso deve incluir o nome do produto que está sendo instalado e um parâmetro de espaço reservado dentro da cadeia de caracteres para o título impresso no disco. Por exemplo, por Microsoft Publisher a propriedade **DiskPrompt** pode ser "Microsoft Publisher: Disco \[ 1", em que 1 é o espaço reservado para o título \] do \[ \] disco.
2.  Insira os títulos de cada um dos discos solicitados em linhas separadas da coluna DiskPrompt da [tabela Mídia.](media-table.md) Por exemplo, a primeira e única entrada na tabela Mídia pode ser "1– Instalar".
3.  Durante a [ação InstallFiles,](installfiles-action.md) o valor da coluna DiskPrompt da tabela [Mídia](media-table.md) é substituído pelo espaço reservado na cadeia de caracteres da [**propriedade DiskPrompt.**](diskprompt.md)
4.  A mensagem exibida pela caixa de mensagem é criada com base em uma cadeia de caracteres de modelo integrado na [tabela Erro](error-table.md). Esse é o Erro 1302 e a cadeia de caracteres de modelo é: "Insira o disco: 2", e o 2 representa um espaço reservado para \[ \] a propriedade \[ \] [**DiskPrompt.**](diskprompt.md)

O exemplo exibe a seguinte mensagem para o usuário: "Insira o disco: Microsoft Publisher: Disco 1 – Instalar".

Observe que as mensagens de prompt de disco são exibidas por todos [os Interface do Usuário,](user-interface-levels.md) exceto Nenhum.

 

 



