---
description: 'Saiba mais sobre: visão geral do banco de dados'
title: Visão geral do banco de dados
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 473ffc7f11b3688f0f0904ae15a366ef7d6812d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566126"
---
# <a name="database-overview"></a>Visão geral do banco de dados


_**Aplica-se a:** Windows | Windows Server_

## <a name="database-overview"></a>Visão geral do banco de dados

O banco de dados ESE é um ISAM (método de acesso sequencial) indexado para armazenamento e recuperação de dado. Um banco de dados ESE é armazenado em um único arquivo e consiste em uma ou mais tabelas definidas pelo usuário. Os dados são organizados em registros na tabela com uma ou mais colunas definidas pelo usuário. Os índices criados fornecem uma organização diferente para todo o conjunto ou um subconjunto de registros na tabela. Usando a API do ESE, os aplicativos podem criar cursores que navegam em registros no banco de dados em diferentes ordens sequenciais. Os elementos da tabela são definidos abaixo:

  - **Coluna**: a coluna é um campo na tabela que armazena um tipo específico de informações. As colunas podem ser fixas ou ter comprimento variável, dependendo do tipo de dados armazenado nelas. Algumas colunas, como colunas marcadas, não ocupam espaço quando **nulas** ou são definidas como o valor padrão e podem conter vários valores.

  - **Registros**: um registro é uma coleção de valores de colunas que têm uma identidade exclusiva, conforme definido pela chave primária.

  - **Index**: o índice é uma coleção de colunas de chave que definem uma ordenação armazenada de registros na tabela. O índice clusterizado ou primário define a ordem na qual os registros são armazenados na tabela. Vários índices podem ser definidos para especificar ordenações diferentes de passagem por meio de registros na tabela. Um índice também pode limitar o conjunto de registros visíveis com base em critérios simples, como a presença ou a ausência de um valor de coluna de chave específico no registro.

  - **Cursor**: o cursor indica o registro atual na tabela e navega para os registros na tabela usando o índice atual. O cursor também contém informações sobre o estado da atualização preparada no momento.

Colunas e índices podem ser adicionados ou removidos da tabela a qualquer momento. Embora vários índices possam ser definidos, os dados na tabela são armazenados fisicamente e logicamente clusterizados de acordo com a definição de índice primário em uma árvore B +. Cada índice secundário é armazenado em uma árvore B + separada que contém apenas ponteiros lógicos para os dados reais que são armazenados na tabela primária. Se nenhum índice for definido, os registros na tabela serão armazenados em uma árvore B + na ordem de inserção e serão referidos como o índice sequencial.

O diagrama aqui é um exemplo de como os dados da tabela são armazenados em uma árvore B + de acordo com o índice primário. O índice primário é para nome e ID, e um índice secundário é criado para o número de escritório do funcionário. As entradas para o índice secundário são armazenadas em uma árvore B + separada que contém somente ponteiros para os registros armazenados na tabela primária. Por exemplo, o número de escritório 12348 na tabela secundária está relacionado ao registro 3 na tabela primária. O registro 3 contém os valores de coluna para o funcionário no Office 12348. Para obter mais informações, consulte o tópico [indexação na tabela](./indexing-in-the-table.md) .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
