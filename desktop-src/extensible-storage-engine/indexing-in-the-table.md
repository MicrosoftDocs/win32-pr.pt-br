---
description: 'Saiba mais sobre: Indexação na tabela'
title: Indexação na tabela
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721446"
---
# <a name="indexing-in-the-table"></a>Indexação na tabela


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="indexing-in-the-table"></a>Indexação na tabela

Um índice é um conjunto de colunas de chave que definem uma ordenação persistente de registros em uma tabela. Os registros são entradas de índice no índice primário. Um índice primário e vários índices secundários podem ser definidos para criar ordens de dados diferentes na tabela.

Embora vários índices possam ser definidos, os registros são armazenados fisicamente em árvores B+ na ordem especificada pelo índice primário. O índice primário é sempre um índice clusterado e também deve ser exclusivo. O índice primário deve ser declarado antes da primeira atualização da tabela para preservar a ordenação do índice. Quando nenhum índice primário é definido pelo aplicativo, os dados são armazenados na ordem em que os registros são adicionados à tabela. Esse índice especial é conhecido como um índice sequencial.

Árvores B+ separadas são usadas para ordenar registros de acordo com o índice secundário. Entradas de índice no índice secundário contêm ponteiros para os dados armazenados de acordo com o índice primário. As entradas de índice para registros no índice primário devem ser exclusivas porque o índice secundário aponta para o registro usando a chave primária do registro. Índices secundários podem ou não ter uma restrição de exclusividade. Para obter mais informações, consulte o tópico [Visão geral do banco de](./database-overview.md) dados.
