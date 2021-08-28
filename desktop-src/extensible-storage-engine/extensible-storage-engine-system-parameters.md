---
description: 'Saiba mais sobre: Parâmetros extensíveis Armazenamento do sistema do mecanismo'
title: Parâmetros do sistema Armazenamento mecanismo extensível
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
ms.openlocfilehash: 501f98ec1b360e3eaa10988c140f30b86dcacb5a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987339"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parâmetros do sistema Armazenamento mecanismo extensível


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-system-parameters"></a>Parâmetros do sistema Armazenamento mecanismo extensível

As constantes a seguir são usadas como valores para o parâmetro *paramid* das funções [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter.](./jetsetsystemparameter-function.md)

  - [Parâmetros de backup e restauração](./backup-and-restore-parameters.md)

  - [Parâmetros de retorno de chamada](./callback-parameters.md)

  - [Parâmetros de Banco de Dados](./database-parameters.md)

  - [Parâmetros de cache do banco de dados](./database-cache-parameters.md)

  - [Parâmetros de tratamento de erro](./error-handling-parameters.md)

  - [Parâmetros do log de eventos](./event-log-parameters.md)

  - [Parâmetros de E/S](./i-o-parameters.md)

  - [Parâmetros de Índice](./index-parameters.md)

  - [Parâmetros informacionais](./informational-parameters.md)

  - [Metadados de parâmetros](./meta-parameters.md)

  - [Parâmetros de recurso](./resource-parameters.md)

  - [Parâmetros de banco de dados temporários](./temporary-database-parameters.md)

  - [Parâmetros de Log de Transação](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato de descrição do parâmetro do sistema

Cada parâmetro do sistema será descrito usando o seguinte formato:

JET_paramX

Descrição do parâmetro JET_paramX sistema.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>O valor padrão do parâmetro.</p> | 
| <p>Tipo:</p> | <p>O tipo de dados do parâmetro.</p> | 
| <p>Intervalo válido:</p> | <p>Os valores legais do parâmetro.</p> | 
| <p>Escopo:</p> | <p>O parâmetro é Global ou por Instância?</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>O parâmetro pode ser definido se existirem instâncias?</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>O parâmetro pode ser definido quando inicializado?</p> | 
| <p>Afeta o layout físico:</p> | <p>O parâmetro afeta os arquivos no disco?</p> | 
| <p>Afeta a confiabilidade:</p> | <p>O parâmetro afeta a confiabilidade do mecanismo?</p> | 
| <p>Afeta o desempenho:</p> | <p>O parâmetro afeta o desempenho do mecanismo?</p> | 
| <p>Afeta recursos:</p> | <p>O parâmetro afeta os recursos do mecanismo?</p> | 
| <p>Disponibilidade:</p> | <p>Versões de Windows que suportam o parâmetro .</p> | 

