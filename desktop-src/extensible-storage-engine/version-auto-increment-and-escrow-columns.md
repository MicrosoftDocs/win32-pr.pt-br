---
description: 'Saiba mais sobre: versões, incremento automático e colunas de caução'
title: Colunas de versão, incremento automático e caução
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765024"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Colunas de versão, incremento automático e caução


_**Aplica-se a:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Colunas de versão, incremento automático e caução

O ESE fornece tipos de coluna de atualização de versão, incremento automático e caução que têm capacidades especiais. As opções de coluna definidas no membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) usada na chamada para [JetAddColumn](./jetaddcolumn-function.md) indicam se a coluna é um dos tipos especializados indicados aqui.

### <a name="version-jet_bitcolumnversion"></a>Versão (JET_bitColumnVersion)

A opção de coluna Version, aplicada somente a JET_coltypLong colunas, indica que a coluna contém informações de versão sobre o registro que podem ser usadas para determinar se uma cópia na memória de um determinado registro precisa ser atualizada. As colunas de versão são incrementadas automaticamente pelo ESE quando a coluna é modificada pelo aplicativo por meio de [JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automático (JET_bitColumnAutoincrement)

As colunas de incremento automático são incrementadas automaticamente pelo ESE quando um novo registro é inserido na tabela. O valor contido na coluna de incremento automático é exclusivo para cada registro na tabela e não é garantido que seja contínuo. Esses valores não são reciclados, mas podem ser reutilizados em determinados casos. Somente colunas do tipo JET_coltypLong e JET_coltypLongLong podem ser colunas de incremento automático.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Caução (JET_bitColumnEscrowUpdate)

Colunas de caução podem ser modificadas na chamada para [JetEscrowUpdate](./jetescrowupdate-function.md). As atualizações na caução são operações Delta numéricas que não sofrem com conflitos de gravação. Isso significa que qualquer número de sessões pode atualizar simultaneamente uma coluna de caução em um registro por meio de [JetEscrowUpdate](./jetescrowupdate-function.md) sem conflitos. Observe que qualquer outra operação de atualização ainda pode resultar em um conflito de gravação com uma operação de atualização de caução. As atualizações de caução só podem ser feitas em colunas do tipo JET_coltypLong que têm um valor padrão. Essas colunas também devem ser adicionadas a uma tabela antes de serem carregadas com linhas. Finalmente, as linhas que contêm uma coluna de atualização de caução podem ser configuradas para dar suporte a um retorno de chamada de finalização de linha (JET_bitColumnFinalize) ou para serem excluídas automaticamente se a contagem de referência chegar a zero (JET_bitColumnDeleteOnZero). Para obter mais informações, consulte a estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) .
