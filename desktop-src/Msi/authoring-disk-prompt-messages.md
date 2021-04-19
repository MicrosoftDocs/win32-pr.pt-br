---
description: Use as diretrizes a seguir para criar um Windows Installer instalação que exibe uma caixa de mensagem solicitando que o usuário insira um disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Criando mensagens de prompt de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747989"
---
# <a name="authoring-disk-prompt-messages"></a>Criando mensagens de prompt de disco

Use as diretrizes a seguir para criar um Windows Installer instalação que exibe uma caixa de mensagem solicitando que o usuário insira um disco.

**Para exibir uma caixa de mensagem solicitando que o usuário insira um disco**

1.  Use os recursos de criação do instalador para definir a cadeia de caracteres da propriedade [**DiskPrompt**](diskprompt.md) na tabela de [Propriedades](property-table.md) . Isso deve incluir o nome do produto que está sendo instalado e um parâmetro de espaço reservado na cadeia de caracteres para o título impresso no disco. Por exemplo, para o Microsoft Publisher, a propriedade **DiskPrompt** poderia ser "Microsoft Publisher: disco \[ 1 \] ", em que \[ 1 \] é o espaço reservado para o título do disco.
2.  Insira os títulos de cada um dos discos que estão sendo solicitados em linhas separadas da coluna DiskPrompt da tabela de [mídia](media-table.md) . Por exemplo, a primeira e única entrada na tabela de mídia poderia ser "1 – instalar".
3.  Durante a ação [InstallFiles](installfiles-action.md) , o valor da coluna DiskPrompt da tabela de [mídia](media-table.md) é substituído pelo espaço reservado na cadeia de caracteres da propriedade [**DiskPrompt**](diskprompt.md) .
4.  A mensagem exibida pela caixa de mensagem é criada a partir de uma cadeia de caracteres de modelo interna na [tabela de erros](error-table.md). Esse é o erro 1302 e a cadeia de caracteres do modelo é: "Insira o disco: \[ 2 \] " e o \[ 2 \] representa um espaço reservado para a propriedade [**DiskPrompt**](diskprompt.md) .

O exemplo exibe a seguinte mensagem para o usuário: "Insira o disco: Microsoft Publisher: disco 1 – instalar."

Observe que as mensagens de prompt de disco são exibidas por todos os [níveis de interface do usuário](user-interface-levels.md) , exceto nenhuma.

 

 



