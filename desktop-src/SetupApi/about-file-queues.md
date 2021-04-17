---
description: Uma fila de arquivos é uma lista de operações de arquivo que são processadas de uma vez. As operações de arquivo na fila podem ser operações de cópia, renomeação ou exclusão. A fila de arquivos organiza as operações de arquivo por tipo, criando cópias, renomear e excluir subfilas.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Sobre filas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751067"
---
# <a name="about-file-queues"></a>Sobre filas de arquivos

Uma fila de arquivos é uma lista de operações de arquivo que são processadas de uma vez. As operações de arquivo na fila podem ser operações de cópia, renomeação ou exclusão. A fila de arquivos organiza as operações de arquivo por tipo, criando cópias, renomear e excluir subfilas.

Essas operações podem ser enviadas para a fila em qualquer ordem, e o processo de enfileiramento não precisa ser contíguo. Quando a fila é confirmada, a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) executa operações de arquivo na ordem do tipo de operação.

Normalmente, todas as operações de arquivo necessárias para uma instalação inteira são enfileiradas na fila de arquivos e, em seguida, processadas em um único lote quando a fila é confirmada.

Uma vantagem de enfileirar operações de arquivo na seção Instalando arquivos por seção de um arquivo INF é que você pode simplificar o processo de instalação. Em vez de ter que obter informações do usuário para que cada seção seja instalada, você pode obter informações de instalação do usuário para todos os arquivos a serem instalados durante a criação da fila. Isso libera o usuário para buscar outras atividades enquanto as operações de cópia com uso intensivo de tempo são processadas pela função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .

Outra vantagem das filas de arquivos é que você pode acompanhar o progresso da instalação como um todo. Ao instalar seções por seção de um arquivo INF, indicadores de progresso como barras de progresso podem rastrear apenas a seção INF atual. Quando a próxima seção for instalada, a barra de progresso será iniciada. Com uma fila, o número total de arquivos a serem processados durante toda a instalação é conhecido antes da fila ser confirmada e, portanto, uma barra de progresso pode ser gerada para rastrear toda a instalação.

Para mais informações, consulte os seguintes tópicos:

-   [Ordem de compromisso de fila](order-of-queue-commitment.md)
-   [Notificações de fila](queue-notifications.md)

 

 



