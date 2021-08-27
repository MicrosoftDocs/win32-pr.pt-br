---
description: 'Saiba mais sobre: função JetDefragment2'
title: Função JetDefragment2
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d31b6203de9feb9301b3c08c01bee84c666a9e9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465833"
---
# <a name="jetdefragment2-function"></a>Função JetDefragment2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdefragment2-function"></a>Função JetDefragment2

A função **JetDefragment2** inicia e interrompe as tarefas de desfragmentação do banco de dados, o que melhora a organização da data em um banco de dado, com um parâmetro de retorno de chamada disponível para relatar o progresso da desfragmentação. Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados. Ele também pode reduzir o conjunto de trabalho, garantindo que os dados sejam mais bem compactados. Por fim, ele pode melhorar o desempenho do aplicativo acelerando as operações comuns por meio de uma melhor organização de dados.

**Windows xp:** o **JetDefragment2** é introduzido no Windows XP.  

**JetDefragment2** também contém um parâmetro de função de retorno de chamada que é usado para relatar o progresso do processo de desfragmentação.

A desfragmentação de banco de dados é uma operação online e não interrompe a atividade de banco de dados regular, como operações de consulta ou atualizações de data. O **JetDefragment2** também não faz uma cópia de todos os dados existentes. Em vez disso, ele desfragmenta um banco de dados em vigor. Por fim, o **JetDefragment2** recupera o espaço interno do banco de dados para reutilização, mas não libera espaço em excesso para o sistema de arquivos do sistema operacional.

O formato resultante dos dados pode ser muito mais eficiente, mas geralmente não é o ideal. A desfragmentação é limitada à liberação de páginas de banco de dados para reutilização que contêm dados que já foram excluídos logicamente. A desfragmentação também torna as páginas de banco de dados disponíveis para reutilização em alguns casos, combinando dados de duas páginas quando elas podem caber em uma única página.

Essa operação é diferente de [JetCompact](./jetcompact-function.md) , que faz uma cópia de um banco de dados somente leitura em um formato altamente ideal.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*DBID*

O banco de dados a ser desfragmentado.

*szTableName*

Às vezes, *szTableName* é necessário e, às vezes, é proibido:

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Deve ser `NULL`. |
| `JET_bitDefragmentBTree` | Especifica o nome da tabela/árvore b a ser desfragmentada. |
| *outros* | Deve ser `NULL`. |
 
A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.

*pcPasses*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o número máximo de passagens de desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido como o número de passagens executadas.

Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.

*pcSeconds*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o tempo máximo para a desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido com o período de tempo usado para a desfragmentação.

Quando esse parâmetro é definido como nulo ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.

*retorno de chamada*

Função de retorno de chamada que a desfragmentação chama regularmente para relatar o progresso.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Deve ser `NULL`. |
| `JET_bitDefragmentBTree` | Deve ser `NULL`. |
| *outros* | Opcional.


*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDefragmentAvailSpaceTreesOnly</p> | <p>Essa opção é usada para desfragmentar a parte de espaço disponível da alocação de espaço do banco de dados ESE. O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível. O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente. O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</p> | 
| <p>JET_bitDefragmentBatchStart</p> | <p>Essa opção é usada para iniciar uma nova tarefa de desfragmentação.</p> | 
| <p>JET_bitDefragmentBatchStop</p> | <p>Essa opção é usada para interromper uma tarefa de desfragmentação iniciada existente.</p> | 
| <p>JET_bitDefragmentBTree</p> | <p>Essa opção é usada para desfragmentar uma árvore B, especificada por szTableName.</p> | 
| <p>JET_bitDefragmentBTreeBatch</p> | <p>Essa opção é usada para chamar OLD2 em todo o banco de dados.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</p> | 
| <p>JET_errDistributedTransactionAlreadyPreparedToCommit</p> | <p>A sessão fornecida está no estado preparado para confirmar e não pode iniciar novas atualizações até que a transação atual seja confirmada ou revertida.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>A ID de banco de dados fornecida não corresponde a um banco de dados conhecido na instância.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A sessão fornecida tem somente privilégios somente leitura e não pode iniciar uma tarefa que possa executar uma atualização, incluindo a desfragmentação.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</p> | 
| <p>JET_wrnDefragAlreadyRunning</p> | <p>A opção JET_bitDefragmentBatchStart foi aprovada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados especificado.</p> | 
| <p>JET_wrnDefragNotRunning</p> | <p>A JET_bitDefragmentBatchStop foi passada, mas nenhuma tarefa de desfragmentação está em execução no momento.</p> | 



Em caso de êxito, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de interromper uma tarefa de desfragmentação existente é executada.

Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita. Nenhum outro efeito colateral ocorre.

#### <a name="remarks"></a>Comentários

A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API. O valor padrão do parâmetro do sistema é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte. No entanto, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilita-la seletivamente somente para árvores de espaço de banco de dados, somente bancos de dados, arquivos de streaming ou qualquer combinação dessas opções. Se a configuração do sistema para desfragmentação online for para uma configuração obsoleta, **JetDefragment2** tratará a configuração como JET_OnlineDefragAll.

Pode haver no máximo uma tarefa em execução para cada banco de dados. A tarefa é executado como um thread no processo que hospeda o ESE.

A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continua, porque a tarefa de desfragmentação aloca sua própria sessão. A sessão determinada só é usada para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as próprias operações de desfragmentação.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
