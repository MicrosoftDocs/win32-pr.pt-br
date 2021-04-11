---
description: 'Saiba mais sobre: função JetBeginTransaction'
title: Função JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296182"
---
# <a name="jetbegintransaction-function"></a>Função JetBeginTransaction


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>Função JetBeginTransaction

A função **JetBeginTransaction** faz com que uma sessão Insira uma transação e crie um novo ponto de salvamento. Essa função pode ser chamada mais de uma vez em uma única sessão para causar a criação de pontos de salvamento adicionais. Esses pontos de salvamento podem ser usados para manter ou descartar de forma seletiva as alterações no estado do banco de dados.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

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
<th><p>Descrição</p></th>
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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>Uma nova transação não pode ser iniciada porque a sessão já está na profundidade máxima de ponto de salvamento permitida pelo mecanismo de banco de dados.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a sessão fornecida estará dentro de uma transação. Se a sessão estava anteriormente dentro de uma transação, um novo ponto de salvamento será criado.

Se houver falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

O mecanismo de banco de dados fornece um modelo de isolamento de instantâneo para suas transações. Isso significa que, quando uma sessão entra pela primeira vez em um estado transacional, a sessão verá todo o banco de dados congelado no início da transação. Uma sessão não precisa ler nenhum dado de bloqueio porque ela sempre pode acessar a versão apropriada desses dados. Isso significa que uma sessão que está atualizando dados nunca bloqueará a leitura desses dados em uma sessão diferente.

Outra implicação do uso de isolamento de instantâneo é o modelo de bloqueio usado para atualizações. O mecanismo de banco de dados oferecerá um bloqueio de gravação em determinado dado para a primeira sessão que o solicita. Esse bloqueio de gravação é liberado quando a transação é confirmada ou anulada completamente, de modo que a sessão não esteja mais em uma transação. Enquanto uma sessão mantém um bloqueio de gravação, qualquer outra sessão que solicite o mesmo bloqueio de gravação não será bloqueada até que o bloqueio de gravação esteja disponível. Em vez disso, essa segunda sessão falhará imediatamente com JET_errWriteConflict. Para resolver esse conflito, a segunda sessão deve anular (ou confirmar) sua transação completamente, aguardar um pequeno período de tempo para a primeira sessão confirmar ou anular sua transação e iniciar tudo novamente.

Para dar suporte ao isolamento de instantâneo, o mecanismo de banco de dados armazena todas as versões de todos os dados modificados na memória desde o momento em que a transação ativa mais antiga em qualquer sessão foi iniciada pela primeira vez. Isso tem implicações importantes para seu aplicativo. Qualquer comportamento que faça com que um grande número de versões para se acumular na memória pode fazer com que a instância esgotasse seu tamanho máximo de repositório de versão (consulte [JET_paramMaxVerPages](./resource-parameters.md) em [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter mais informações). Esse comportamento inclui, mas não se limita a atualizações muito grandes em uma única transação e transações de execução muito longa. Como resultado, é muito importante configurar corretamente o tamanho do repositório de versão para a carga transacional esperada do aplicativo. Também é importante tomar muito cuidado para limitar o número de atualizações executadas em uma única transação. Além disso, é importante tornar as transações tão curtas quanto possível em cenários de alta carga.

É altamente recomendável que o aplicativo sempre esteja no contexto de uma transação ao chamar as APIs do ESE que recuperam ou atualizam dados. Se isso não for feito, o mecanismo de banco de dados encapsulará automaticamente cada chamada à API do ESE desse tipo em uma transação em nome do aplicativo. O custo dessas transações muito curtas pode ser somado rapidamente em alguns casos.

O comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread a partir do momento em que a primeira chamada para **JetBeginTransaction** é feita até o momento em que a chamada de correspondência para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita. Esse comportamento pode ser alterado para remover essa restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

O mecanismo de banco de dados também dá suporte a modificações de esquema transacionais. Por exemplo, é possível iniciar uma nova transação, criar uma tabela, adicionar algumas colunas, criar um índice ou dois e, em seguida, anular a transação. Os elementos de esquema que acabou de ser adicionados serão removidos do banco de dados. Também é possível misturar modificações de esquema e atualizações de banco de dados comuns na mesma transação.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
