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
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105816038"
---
# <a name="jetdefragment2-function"></a>Função JetDefragment2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>Função JetDefragment2

A função **JetDefragment2** inicia e interrompe as tarefas de desfragmentação do banco de dados, o que melhora a organização da data em um banco de dado, com um parâmetro de retorno de chamada disponível para relatar o progresso da desfragmentação. Isso é feito para limitar o crescimento do banco de dados usando a alocação de disco existente com mais eficiência no banco de dados. Ele também pode reduzir o conjunto de trabalho, garantindo que os dados sejam mais bem compactados. Por fim, ele pode melhorar o desempenho do aplicativo acelerando as operações comuns por meio de uma melhor organização de dados.

**Windows XP:** o **JetDefragment2** é introduzido no Windows XP.  

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

Parâmetro não utilizado. A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.

*pcPasses*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o número máximo de passagens de desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido como o número de passagens executadas.

Quando esse parâmetro é definido como NULL, o número de passagens de desfragmentação online é ilimitado.

*pcSeconds*

Ao iniciar uma tarefa de desfragmentação online, esse parâmetro de entrada opcional define o tempo máximo para a desfragmentação. Ao parar uma tarefa de desfragmentação online, esse buffer de saída opcional é definido com o período de tempo usado para a desfragmentação.

Quando esse parâmetro é definido como nulo ou se *pcSeconds* aponta para um valor negativo, o tempo máximo para desfragmentação é ilimitado.

*retorno de chamada*

Função de retorno de chamada que a desfragmentação chama regularmente para relatar o progresso.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Essa opção é usada para desfragmentar a parte de espaço disponível da alocação de espaço do banco de dados ESE. O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível. O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente. O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Essa opção é usada para iniciar uma nova tarefa de desfragmentação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Essa opção é usada para interromper uma tarefa de desfragmentação iniciada existente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Essa opção é usada para desfragmentar uma árvore B.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>O banco de dados escolhido para desfragmentação é somente leitura e não pode ser atualizado de nenhuma forma, incluindo a desfragmentação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>A sessão fornecida está no estado preparado para confirmar e não pode iniciar novas atualizações até que a transação atual seja confirmada ou revertida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>A ID de banco de dados fornecida não corresponde a um banco de dados conhecido na instância.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>A sessão fornecida tem somente privilégios somente leitura e não pode iniciar uma tarefa que possa executar uma atualização, incluindo a desfragmentação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Esse erro ocorrerá quando o tamanho configurado do repositório de versão for insuficiente para manter todas as atualizações pendentes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>A opção JET_bitDefragmentBatchStart foi aprovada, mas uma tarefa de desfragmentação já está executando a desfragmentação no banco de dados especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>A opção JET_bitDefragmentBatchStop foi aprovada, mas nenhuma tarefa de desfragmentação está em execução no momento.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a ação solicitada de iniciar uma tarefa de desfragmentação para determinados dados com determinadas opções é executada ou a ação de parar uma tarefa de desfragmentação existente é executada.

Em caso de falha, a ação solicitada de iniciar ou parar um trabalho de desfragmentação online não é feita. Nenhum outro efeito colateral ocorre.

#### <a name="remarks"></a>Comentários

A desfragmentação online é controlada por uma configuração de parâmetro, bem como por essa API. O valor do parâmetro do sistema padrão é JET_OnlineDefragAll, o que significa que a desfragmentação está habilitada para todas as estruturas de dados com suporte. No entanto, usando o [JetSetSystemParameter](./jetsetsystemparameter-function.md), é possível desabilitar a desfragmentação online ou habilitá-la seletivamente somente para árvores de espaço de banco de dados, somente para bancos, somente para arquivos de streaming ou qualquer combinação dessas opções. Se a configuração do sistema para desfragmentação online for para uma configuração obsoleta, **JetDefragment2** tratará a configuração como JET_OnlineDefragAll.

Pode haver, no máximo, uma tarefa em execução para cada banco de dados. A tarefa é executada como um thread no processo que hospeda o ESE.

A sessão usada para iniciar a tarefa de desfragmentação online pode ser usada posteriormente para operações de banco de dados enquanto a tarefa de desfragmentação continuar, pois a tarefa de desfragmentação aloca sua própria sessão. A sessão fornecida é usada apenas para verificar as permissões associadas à sessão de início da tarefa e não é realmente usada para as operações de desfragmentação propriamente ditas.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetDefragment2W</strong> (Unicode) e <strong>JetDefragment2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
