---
description: Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a função GetNPPBlobTable. Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada por seu aplicativo para selecionar a NIC na qual você está interessado.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Selecionando uma NIC de uma tabela de BLOB NPP retornada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828422"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a>Selecionando uma NIC de uma tabela de BLOB NPP retornada

Para selecionar uma NIC de uma tabela de BLOB NPP retornada por Monitor de Rede, chame a função [**GetNPPBlobTable**](getnppblobtable.md) . Essa função retorna uma tabela de BLOB NPP, que pode ser enumerada por seu aplicativo para selecionar a NIC na qual você está interessado.

Ao chamar essa função, você pode retornar uma tabela de BLOB de todas as NICs registradas no computador local ou em um conjunto menor de NICs filtradas. Para filtrar as NICs que são retornadas, você pode fornecer um [*blob de filtro*](f.md) quando a chamada é feita.



| Para obter informações sobre                                                       | Consulte                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Como especificar um filtro que limita as NICs retornadas em uma tabela de BLOB NPP. | [Especificando um BLOB de filtro](specifying-a-filter-blob.md)                                             |
| Como selecionar uma NIC registrada em um computador local.                         | [Selecionando uma NIC registrada](selecting-a-registered-nic.md)                                         |
| Como selecionar uma NIC de uma tabela de BLOB NPP fornecida                          | [Selecionando uma NIC de uma tabela de BLOB NPP fornecida](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



