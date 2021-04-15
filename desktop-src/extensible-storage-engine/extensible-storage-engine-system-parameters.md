---
description: 'Saiba mais sobre: parâmetros do sistema do mecanismo de armazenamento extensível'
title: Parâmetros do sistema do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502301"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parâmetros do sistema do mecanismo de armazenamento extensível


_**Aplica-se a:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>Parâmetros do sistema do mecanismo de armazenamento extensível

As constantes a seguir são usadas como valores para o parâmetro *paramid* das funções [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

  - [Parâmetros de backup e restauração](./backup-and-restore-parameters.md)

  - [Parâmetros de retorno de chamada](./callback-parameters.md)

  - [Parâmetros de Banco de Dados](./database-parameters.md)

  - [Parâmetros de cache do banco de dados](./database-cache-parameters.md)

  - [Parâmetros de tratamento de erros](./error-handling-parameters.md)

  - [Parâmetros do log de eventos](./event-log-parameters.md)

  - [Parâmetros de e/s](./i-o-parameters.md)

  - [Parâmetros de Índice](./index-parameters.md)

  - [Parâmetros informativos](./informational-parameters.md)

  - [Parâmetros meta](./meta-parameters.md)

  - [Parâmetros do recurso](./resource-parameters.md)

  - [Parâmetros de banco de dados temporários](./temporary-database-parameters.md)

  - [Parâmetros de Log de Transação](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato de descrição do parâmetro do sistema

Cada parâmetro do sistema será descrito usando o seguinte formato:

JET_paramX

Descrição do parâmetro do sistema JET_paramX.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>O valor padrão do parâmetro.</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>O tipo de dados do parâmetro.</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Os valores válidos para o parâmetro.</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>O parâmetro é global ou por instância?</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>O parâmetro pode ser definido se existir alguma instância?</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>O parâmetro pode ser definido quando inicializado?</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>O parâmetro afeta os arquivos em disco?</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>O parâmetro afeta a confiabilidade do mecanismo?</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>O parâmetro afeta o desempenho do mecanismo?</p></td>
</tr>
<tr class="even">
<td><p>Afeta os recursos:</p></td>
<td><p>O parâmetro afeta os recursos do mecanismo?</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Versões do Windows que dão suporte ao parâmetro.</p></td>
</tr>
</tbody>
</table>
