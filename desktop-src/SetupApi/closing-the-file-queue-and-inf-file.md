---
description: Depois que a fila terminar de confirmar suas operações, ela deverá ser fechada usando a função SetupCloseFileQueue com o identificador que foi criado pelo SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Fechando a fila de arquivos e o arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769183"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Fechando a fila de arquivos e o arquivo INF

Depois que a fila terminar de confirmar suas operações, ela deverá ser fechada usando a função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) com o identificador que foi criado pelo [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). O retorno de chamada da fila padrão deve ser destruído e recriado para que outra fila possa ser confirmada.

Se um contexto padrão foi iniciado para uso pela rotina de retorno de chamada padrão, ele também deve ser encerrado chamando a função [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) . O *contexto* é um ponteiro para a estrutura retornada pela função [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .

Quando o acesso às informações de INF não for mais necessário, chame a função [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) com o identificador que foi criado pelo [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) para liberar recursos do sistema.

 

 



