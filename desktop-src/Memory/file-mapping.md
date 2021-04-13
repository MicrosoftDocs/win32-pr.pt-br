---
description: O mapeamento de arquivo é a associação do conteúdo de um arquivo com uma parte do espaço de endereço virtual de um processo.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Mapeamento de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501761"
---
# <a name="file-mapping"></a>Mapeamento de arquivo

O *mapeamento de arquivo* é a associação do conteúdo de um arquivo com uma parte do espaço de endereço virtual de um processo. O sistema cria um *objeto de mapeamento de arquivo* (também conhecido como um *objeto de seção*) para manter essa associação. Uma *exibição de arquivo* é a parte do espaço de endereço virtual que um processo usa para acessar o conteúdo do arquivo. O mapeamento de arquivo permite que o processo use e/s (entrada e saída) aleatória e e/s sequencial. Ele também permite que o processo funcione com eficiência com um arquivo de dados grande, como um banco de dado, sem a necessidade de mapear o arquivo inteiro na memória. Vários processos também podem usar arquivos mapeados por memória para compartilhar dados.

Processa a leitura e gravação na exibição de arquivo usando ponteiros, assim como faria com memória alocada dinamicamente. O uso do mapeamento de arquivos melhora a eficiência porque o arquivo reside no disco, mas a exibição do arquivo reside na memória. Os processos também podem manipular a exibição de arquivo com a função [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) .

A ilustração a seguir mostra a relação entre o arquivo em disco, um objeto de mapeamento de arquivo e uma exibição de arquivo.

![relação entre o arquivo no disco, um objeto de mapeamento de arquivo e uma exibição de arquivo.](images/fmap.png)

O arquivo no disco pode ser qualquer arquivo que você deseja mapear na memória ou pode ser o arquivo de página do sistema. O objeto de mapeamento de arquivo pode consistir em apenas parte do arquivo ou apenas. Ele é apoiado pelo arquivo em disco. Isso significa que, quando o sistema troca páginas do objeto de mapeamento de arquivo, todas as alterações feitas no objeto de mapeamento de arquivo são gravadas no arquivo. Quando as páginas do objeto de mapeamento de arquivo são trocadas novamente, elas são restauradas do arquivo.

Um modo de exibição de arquivo pode consistir em apenas parte do objeto de mapeamento de arquivo. Um processo manipula o arquivo por meio de exibições de arquivo. Um processo pode criar várias exibições para um objeto de mapeamento de arquivo. As exibições de arquivo criadas por cada processo residem no espaço de endereço virtual desse processo. Quando o processo precisa de dados de uma parte do arquivo que não seja o que está na exibição de arquivo atual, ele pode desmapear a exibição de arquivo atual e, em seguida, criar uma nova exibição de arquivo.

Quando vários processos usam o mesmo objeto de mapeamento de arquivo para criar exibições para um arquivo local, os dados são coerentes. Ou seja, as exibições contêm cópias idênticas do arquivo no disco. O arquivo não pode residir em um computador remoto se você quiser compartilhar memória entre vários processos.

Para mais informações, consulte os seguintes tópicos:

-   [Criando um objeto de mapeamento de arquivo](creating-a-file-mapping-object.md)
-   [Criando uma exibição de arquivo](creating-a-file-view.md)
-   [Compartilhando arquivos e memória](sharing-files-and-memory.md)
-   [Leitura e gravação de uma exibição de arquivo](reading-and-writing-from-a-file-view.md)
-   [Fechando um objeto de mapeamento de arquivo](closing-a-file-mapping-object.md)
-   [Segurança de mapeamento de arquivo e direitos de acesso](file-mapping-security-and-access-rights.md)
-   [Usando mapeamento de arquivo](using-file-mapping.md)

 

 
