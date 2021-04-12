---
description: Limita os recursos internos que são usados por operações iniciadas por clientes WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: Classe __ArbitratorConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170196"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_Classe ArbitratorConfiguration

A classe **\_ \_ ArbitratorConfiguration** é uma classe de configuração que limita os recursos internos que são usados por operações iniciadas por clientes WMI. Essa é uma classe singleton que reside no \\ namespace raiz. A classe é gerada internamente para que não haja nenhum arquivo MOF para ela.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ ArbitratorConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ ArbitratorConfiguration** tem essas propriedades.

<dl> <dt>

**OutstandingTasksPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número de tarefas de usuário pendentes iniciadas a qualquer momento.

</dd> <dt>

**OutstandingTasksTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número total de tarefas pendentes a qualquer momento.

</dd> <dt>

**PermanentSubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de assinaturas permanentes permitidas para um usuário específico a qualquer momento.

</dd> <dt>

**PermanentSubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de assinaturas permanentes permitidas para todos os usuários a qualquer momento.

</dd> <dt>

**PollingInstructionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de consultas de evento de sondagem permitidas para um usuário específico a qualquer momento.

</dd> <dt>

**PollingInstructionsTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de instruções de sondagem permitidas para todos os usuários a qualquer momento.

</dd> <dt>

**PollingMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de consultas de eventos de sondagem de memória, emitidas por um usuário específico, pode consumir a qualquer momento.

</dd> <dt>

**PollingMemoryTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade total de memória que sonda consultas de eventos, para todos os usuários combinados, pode ser consumidora a qualquer momento.

</dd> <dt>

**QuotaRetryCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número de violações de cota permitidas antes que uma tarefa seja cancelada.

</dd> <dt>

**QuotaRetryWaitInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Atraso introduzido na execução da tarefa em cada violação de cota.

</dd> <dt>

**TaskThreadsPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número máximo de threads de tarefa associados a um usuário específico t qualquer vez.

</dd> <dt>

**TaskThreadsTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número máximo de threads de tarefa.

</dd> <dt>

**TemporarySubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de assinaturas temporárias permitidas para um usuário específico a qualquer momento.

</dd> <dt>

**TemporarySubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número total de assinaturas temporárias permitidas para todos os usuários a qualquer momento.

</dd> <dt>

**TotalCacheDisk**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Total de cache de disco associado a todos os usuários a qualquer momento.

</dd> <dt>

**TotalCacheDiskPerTask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Total de cache de disco associado a uma tarefa específica a qualquer momento.

</dd> <dt>

**TotalCacheDiskPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Total de cache de disco associado a um usuário específico a qualquer momento.

</dd> <dt>

**TotalCacheMemory**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Total de cache de memória associado a todos os usuários de uma vez.

</dd> <dt>

**TotalCacheMemoryPerTask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Cache de memória total associado a uma tarefa específica a qualquer momento.

</dd> <dt>

**TotalCacheMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Total de cache de memória associado a um usuário específico em qualquer momento.

</dd> <dt>

**TotalUsers**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não utilizado. Número máximo de usuários conectados.

</dd> </dl>

## <a name="remarks"></a>Comentários

**\_ \_ ArbitratorConfiguration** é herdado de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

