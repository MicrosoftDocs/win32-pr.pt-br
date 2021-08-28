---
description: 'Saiba mais sobre: Função JetDefragment'
title: Função JetDefragment
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f9fdce5268e6981fa018f58ed14b31c2c078cce
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985940"
---
# <a name="jetdefragment-function"></a>Função JetDefragment


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdefragment-function"></a>Função JetDefragment

A **função JetDefragment** inicia e interrompe tarefas de desfragmentação de banco de dados que melhoram a organização de dados em um banco de dados. Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados. Ele também pode reduzir o conjunto de trabalho garantindo que os dados são empacotados mais de perto. Por fim, ele pode melhorar o desempenho do aplicativo acelerando operações comuns por meio de uma melhor organização de dados.

A desfragmentação de banco de dados é uma operação online e não interrompe a atividade regular do banco de dados, como operações de consulta ou atualizações de dados. **JetDefragment** também não faz uma cópia de todos os dados existentes. Em vez disso, ele desfragmenta um banco de dados no local. Por fim, **JetDefragment** recupera espaço interno do banco de dados para rea uso, mas não libera espaço em excesso para o sistema de arquivos do sistema operacional.

O formato resultante dos dados pode ser muito mais eficiente, mas geralmente não é ideal. A desfragmentação está limitada à liberação de páginas de banco de dados para rea utilização que contêm dados que já foram excluídos logicamente. A desfragmentação também disponibiliza páginas de banco de dados para reajuste em alguns casos combinando dados de duas páginas quando ele pode caber em uma única página.

Essa operação é diferente do [JetCompact,](./jetcompact-function.md) que faz uma cópia de um banco de dados somente leitura em uma forma altamente ideal.

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Dbid*

O banco de dados que será desfragmentado.

*szTableName*

Parâmetro não usado. A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados determinada.

*pcPasses*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada define o número máximo de passagens de desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido como o número de passagens executadas.

Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.

*pcSeconds*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada define o tempo máximo para desfragmentação. Ao interromper uma tarefa de desfragmentação online, esse buffer de saída é definido como o período de tempo usado para desfragmentação.

Quando esse parâmetro é definido como NULL ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Desfragmenta a parte de espaço disponível da alocação de espaço do banco de dados ESE. O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível. O espaço de propriedade é alocado a uma tabela ou índice enquanto o espaço disponível está pronto para uso na tabela ou índice, respectivamente. O espaço disponível é muito mais dinâmico no comportamento e requer desfragmentação online mais do que o espaço ou dados de tabela ou índice de propriedade.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Inicia uma nova tarefa de desfragmentação.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Interrompe uma tarefa de desfragmentação.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>A sessão determinada está no estado preparado para confirmação e não pode iniciar novas atualizações até que a transação atual seja comprometida ou retida.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>A ID de banco de dados determinada não é igual a um banco de dados conhecido na instância.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A sessão determinada tem privilégios somente leitura e não pode iniciar uma tarefa que pode executar uma atualização, incluindo desfragmentação.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Esse erro ocorrerá quando o tamanho configurado do armazenamento de versão for insuficiente para armazenar todas as atualizações pendentes.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>A JET_bitDefragmentBatchStart foi passada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados determinado.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>A JET_bitDefragmentBatchStop foi passada, mas nenhuma tarefa de desfragmentação está em execução no momento.</p> | 



Em caso de êxito, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de interromper uma tarefa de desfragmentação existente é executada.

Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita. Nenhum outro efeito colateral ocorre.

#### <a name="remarks"></a>Comentários

A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API. O valor padrão do parâmetro do sistema é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte. No entanto, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilita-la seletivamente somente para árvores de espaço de banco de dados, somente bancos de dados, arquivos de streaming ou qualquer combinação dessas opções. Se a configuração do sistema para desfragmentação online estiver definida como uma configuração obsoleta, **JetDefragment** tratará a configuração como JET_OnlineDefragAll.

Pode haver no máximo uma tarefa em execução para cada banco de dados. A tarefa é executado como um thread no processo que hospeda o ESE.

A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continua, porque a tarefa de desfragmentação aloca sua própria sessão. A sessão determinada só é usada para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as próprias operações de desfragmentação.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDefragmentW</strong> (Unicode) e <strong>JetDefragmentA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment2](./jetdefragment2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
