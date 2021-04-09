---
description: 'Saiba mais sobre: colunas de valor longo'
title: Colunas de valor longo
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010396"
---
# <a name="long-value-columns"></a>Colunas de valor longo


_**Aplica-se a:** Windows | Windows Server_

## <a name="long-value-columns"></a>Colunas de valor longo

Os tipos de coluna ESE JET_coltypLongText e JET_coltypLongBinary são chamados de tipos de coluna de valor longo. Essas colunas são grandes cadeias de caracteres e objetos binários grandes que podem ser armazenados em árvores B + separadas fora do índice primário. Quando valores longos são armazenados separados do registro primário, eles são internamente inseridos em uma ID de valor longo (tampa) e em um deslocamento de bytes e acessados como um fluxo. Colunas de valor longo são adicionadas à tabela na chamada de [JetAddColumn](./jetaddcolumn-function.md) com o membro **coltyp** da estrutura de [JET_COLUMNDEF](./jet-columndef-structure.md) definida como JET_coltypLongText ou JET_coltypLongBinary. O tamanho máximo de um valor longo ou de coluna binária longa é 2 GB-1.

O ESE dá suporte a operações de acréscimo, substituição de intervalo de bytes e definição de tamanho para colunas de valor longo para dar suporte a implementações de fluxo eficientes nesses tipos de coluna. Por padrão, os dados de valor longo são armazenados em uma árvore B + separada se ele for maior que 1024 bytes ou se o registro não couber em uma única página de banco de dados quando o valor longo for armazenado no registro. O aplicativo tem a opção de substituir o comportamento padrão definindo opções para armazenar dados de valor longo no registro (JET_bitSetIntrinsicLV) ou forçá-los a serem armazenados na árvore B + separada (JET_bitSetIntrinsicLV). Esses valores são definidos no parâmetro *grbit* em [JetSetColumn](./jetsetcolumn-function.md), ou o membro **grbit** [JET_SETCOLUMN](./jet-setcolumn-structure.md) usado na chamada para [JetSetColumns](./jetsetcolumns-function.md) da seguinte maneira:

  - Acrescentar: (JET_bitSetAppendLV)

  - Substituição de intervalo de bytes: (JET_bitSetOverwriteLV)

  - Definir tamanho: (JET_bitSetSizeLV)

  - Forçar separado: (JET_bitSetSeparateLV)

  - Armazenar no registro: (JET_bitSetIntrinsicLV)

Os dados de valor longo são definidos indicando o deslocamento no blob de valor longo e o comprimento dos dados de valor longo no BLOB. O deslocamento para o blob de valor longo é definido no membro **ibLongValue** da estrutura de [JET_SETINFO](./jet-setinfo-structure.md) (para [JetSetColumn](./jetsetcolumn-function.md)) ou no membro **IbLongValue** da estrutura de [JET_SETCOLUMN](./jet-setcolumn-structure.md) (para [JetSetColumns](./jetsetcolumns-function.md)). O membro **pvData** de [JET_SETCOLUMN](./jet-setcolumn-structure.md)e o parâmetro *pvData* na chamada para [JetSetColumn](./jetsetcolumn-function.md) contém os dados de valor longo. As atualizações para colunas de valor longo devem ser executadas dentro de uma transação.

Os dados de valor longo sempre são armazenados em uma tabela separada quando o aplicativo define o JET_bitSetSeparateLV ou o JET_bitSetIntrinsicLV, caso contrário, ele é uma decisão heurística. O ESE armazena o valor longo separado se for maior que 1024 bytes ou se o registro não couber em uma única página de banco de dados, se estiver armazenado em registro.

O diagrama a seguir mostra os dados de valor longo armazenados em uma tabela separada. Quando um valor longo é armazenado fora do registro, uma nova ID de valor longo é criada para se referir ao seu valor. Isso permite que vários registros façam referência ao mesmo valor de coluna. As contagens de referência para os dados serão aumentadas se mais de um registro nos dados apontar para os mesmos dados de valor longo.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

O ESE também dá suporte a um recurso de repositório de instância única que permite que vários registros façam referência ao mesmo objeto binário grande, como embora cada registro tenha sua própria cópia das informações; evitando assim cópias duplicadas dos dados do valor da coluna. Esse recurso é habilitado na chamada para [JetPrepareUpdate](./jetprepareupdate-function.md) com a opção JET_prepInsertCopy definida no parâmetro *Prep* .
