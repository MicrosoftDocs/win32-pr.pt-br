---
description: 'Saiba mais sobre: Colunas de Versão, Incremento Automático e Escrow'
title: Colunas version, auto-increment e escrow
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: b86b37663f7968ad77874ebcc7b2d0f8fd569cc265424bc36feeecccb6d7e148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471276"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Colunas version, auto-increment e escrow


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="version-auto-increment-and-escrow-columns"></a>Colunas version, auto-increment e escrow

O ESE fornece tipos de coluna de atualização de versão, incremento automático e escrow que têm habilidades especiais. As opções de coluna definidas no **membro grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) usadas na chamada para [JetAddColumn](./jetaddcolumn-function.md) indicam se a coluna é um dos tipos especializados indicados aqui.

### <a name="version-jet_bitcolumnversion"></a>Versão (JET_bitColumnVersion)

A opção de coluna de versão, aplicada somente JET_coltypLong colunas, indica que a coluna contém informações de versão sobre o registro que pode ser usado para determinar se uma cópia na memória de um determinado registro precisa ser atualizada. As colunas de versão são incrementadas automaticamente pelo ESE quando a coluna é modificada pelo aplicativo por meio [de JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automático (JET_bitColumnAutoincrement)

As colunas de incremento automático são incrementadas automaticamente pelo ESE quando um novo registro é inserido na tabela. O valor contido na coluna de incremento automático é exclusivo para cada registro na tabela e não tem garantia de ser contínuo. Esses valores não são reciclados, mas podem ser reutilizados em determinados casos. Somente colunas do tipo JET_coltypLong e JET_coltypLongLong podem ser colunas de incremento automático.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Escrow (JET_bitColumnEscrowUpdate)

As colunas de escrow podem ser modificadas na chamada para [JetEscrowUpdate](./jetescrowupdate-function.md). As atualizações no escrow são operações delta numéricas que não sofrem conflitos de gravação. Isso significa que qualquer número de sessões pode atualizar simultaneamente uma coluna de escrow em um registro por meio de [JetEscrowUpdate](./jetescrowupdate-function.md) sem conflitos. Observe que qualquer outra operação de atualização ainda pode resultar em um conflito de gravação com uma operação de atualização de escrow. As atualizações de escrow só podem ser feitas em colunas do tipo JET_coltypLong que têm um valor padrão. Essas colunas também devem ser adicionadas a uma tabela antes de serem carregadas com linhas. Por fim, as linhas que contêm uma coluna de atualização de escrow podem ser configuradas para dar suporte a um retorno de chamada de finalização de linha (JET_bitColumnFinalize) ou ser excluídas automaticamente se a contagem de referência atingir zero (JET_bitColumnDeleteOnZero). Para obter mais informações, consulte a [estrutura JET_COLUMNDEF](./jet-columndef-structure.md) dados.
