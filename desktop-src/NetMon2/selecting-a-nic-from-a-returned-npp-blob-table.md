---
description: Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a função GetNPPBlobTable. Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada pelo seu aplicativo para selecionar a NIC na qual você está interessado.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selecionando uma NIC em uma tabela de BLOB NPP retornada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5555e68e04886b390a6b6bd1f9f8372202fe970a4784ffa2652a3fc991c4da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074466"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a>Selecionando uma NIC em uma tabela de BLOB NPP retornada

Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a [**função GetNPPBlobTable.**](getnppblobtable.md) Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada pelo seu aplicativo para selecionar a NIC na qual você está interessado.

Ao chamar essa função, você pode retornar uma tabela BLOB de todas as NICs registradas no computador local ou um conjunto menor de NICs filtradas. Para filtrar as NICs retornadas, você pode fornecer um [*BLOB de filtro*](f.md) quando a chamada for feita.



| Para obter informações sobre                                                       | Consulte                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Como especificar um filtro que limita as NICs retornadas em uma tabela NPP BLOB. | [Especificando um BLOB de filtro](specifying-a-filter-blob.md)                                             |
| Como selecionar uma NIC registrada em um computador local.                         | [Selecionando uma NIC registrada](selecting-a-registered-nic.md)                                         |
| Como selecionar uma NIC de uma tabela de BLOB NPP fornecida                          | [Selecionando uma NIC em uma tabela de BLOB NPP fornecida](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



