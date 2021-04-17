---
description: Enfileirar as operações de arquivo é útil porque permite processar a instalação como um todo, em vez de por meio da seção INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Criando uma fila e enfileirando operações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755943"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Criando uma fila e enfileirando operações de arquivo

Enfileirar as operações de arquivo é útil porque permite processar a instalação como um todo, em vez de por meio da seção INF.

Para criar uma fila de arquivos, declare uma variável para armazenar o identificador de fila e, em seguida, chame a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) . Depois que a fila é criada, você pode enfileirar as operações de copiar, renomear e excluir, bem como examinar a fila de arquivos para verificar as operações enfileiradas.

Para adicionar operações de arquivo único à fila, use as funções [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)e [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .

Todas as operações de arquivo listadas em uma seção **copiar** arquivos, **Excluir arquivos** ou **renomear arquivos** podem ser adicionadas à fila usando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)ou [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivamente.

Outra maneira de enfileirar todos os arquivos nas seções **copiar arquivos** listadas em uma seção de **instalação** de um inf é usar a função [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

O exemplo a seguir usa a função [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) para enfileirar operações de cópia para todos os arquivos listados em uma seção **copiar arquivos** de um arquivo inf.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

No exemplo, MyQueue é a fila para a qual adicionar operações de cópia, "A: \\ " especifica o caminho para a origem e MyInf é o identificador para o arquivo inf aberto. O parâmetro *ListInfHandle* é definido como **NULL**, indicando que a seção para cópia está em MyInf. MySection é a seção em MyInf que contém os arquivos a serem colocados em fila para cópia.

A cópia do SP de sinalizadores \_ \_ noSkip e a cópia do SP \_ \_ não navegar foram combinadas usando um operador OR para indicar que o usuário não deve receber opções para ignorar ou procurar arquivos se ocorrerem erros.

 

 



