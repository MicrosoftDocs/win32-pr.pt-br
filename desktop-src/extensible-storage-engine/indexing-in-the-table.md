---
description: 'Saiba mais sobre: indexação na tabela'
title: Indexação na tabela
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010615"
---
# <a name="indexing-in-the-table"></a>Indexação na tabela


_**Aplica-se a:** Windows | Windows Server_

## <a name="indexing-in-the-table"></a>Indexação na tabela

Um índice é um conjunto de colunas de chave que definem uma ordenação persistente de registros em uma tabela. Registros são entradas de índice no índice primário. Um índice primário e vários índices secundários podem ser definidos para criar diferentes ordens de dados na tabela.

Embora vários índices possam ser definidos, os registros são fisicamente armazenados em árvores B + na ordem especificada pelo índice primário. O índice primário é sempre um índice clusterizado e também deve ser exclusivo. O índice primário deve ser declarado antes da primeira atualização da tabela para preservar a ordenação do índice. Quando nenhum índice primário é definido pelo aplicativo, os dados são armazenados na ordem em que os registros são adicionados à tabela. Esse índice especial é conhecido como um índice sequencial.

Separe as árvores B + usadas para ordenar registros de acordo com o índice secundário. As entradas de índice no índice secundário contêm ponteiros para os dados armazenados de acordo com o índice primário. As entradas de índice para registros no índice primário devem ser exclusivas porque o índice secundário aponta para o registro usando a chave primária do registro. Os índices secundários podem ou não ter uma restrição de exclusividade. Para obter mais informações, consulte o tópico [visão geral do banco de dados](./database-overview.md) .
