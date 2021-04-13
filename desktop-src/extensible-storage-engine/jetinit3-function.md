---
description: 'Saiba mais sobre: função JetInit3'
title: Função JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297733"
---
# <a name="jetinit3-function"></a>Função JetInit3


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetinit3-function"></a>Função JetInit3

A função **JetInit3** coloca o mecanismo de banco de dados em um estado no qual ele pode dar suporte ao uso do aplicativo de arquivos de banco de dados. O mecanismo já deve estar configurado corretamente para inicialização, o que você realiza usando a função [JetSetSystemParameter](./jetsetsystemparameter-function.md) . Observe que a recuperação de falhas do banco de dados ocorre automaticamente como parte do processo de inicialização.

**Windows Vista:** o **JetInit3** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*pinstance*

A instância que você usa para uma chamada específica. O uso desse parâmetro depende do modo de operação do mecanismo. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000), no qual apenas uma instância tem suporte, você poderá definir esse parâmetro como **NULL** ou como um buffer de saída válido contendo **NULL** ou JET_instanceNil, que retorna o identificador de instância global criado como um efeito colateral da inicialização. Esse identificador de instância pode então ser passado para qualquer outra API que usa uma instância. Se o mecanismo estiver operando no modo de várias instâncias, você deverá definir esse parâmetro como um buffer de entrada válido que contenha o identificador de instância retornado pela função [JetCreateInstance](./jetcreateinstance-function.md) que está sendo inicializada.

*prstInfo*

Parâmetros de recuperação adicionais usados para remapear bancos de dados durante a recuperação, para definir a posição em que a recuperação será interrompida ou para determinar o status de recuperação atual.

*grbit*

Um grupo de bits que especifica zero ou mais das opções listadas e definidas na tabela a seguir.

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
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Este valor está reservado para uso futuro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Este valor está reservado para uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Esse valor permite que o usuário execute a recuperação em um conjunto de arquivos de log, mesmo na ausência dos bancos de dados que foram anexados ao arquivo de log definido em algum momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Esse valor permite que o usuário execute a recuperação, mas apenas até (e não incluindo) a fase de desfazer. Usando esse valor, os logs de transações adicionais podem ser copiados e aplicados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Esse valor faz com que os arquivos de log sejam truncados durante uma recuperação de software bem-sucedida.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Esse valor faz com que uma entrada de mapa de banco de dados ausente seja padrão para o mesmo local.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Esse valor faz com que os logs perdidos do final do fluxo de log sejam ignorados durante uma recuperação.</p>
<p><strong>Windows 7: o JET_bitReplayIgnoreLostLogs</strong> é introduzido no Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para a função **JetInit3** antes que possa ser usada por algo diferente da função [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando a função [JetInit](./jetinit-function.md) . Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações. Observe que [JetTerm](./jetterm-function.md) não deve ser chamado se a função **JetInit3** falhar. No entanto, [JetTerm](./jetterm-function.md) ainda deve ser chamado para todas as instâncias criadas por **JetCreateInstance2** se **JetInit3** nunca foi chamado ou se **JetInit3** tiver êxito.

Se a recuperação estiver em execução em um conjunto de logs para os quais nem todos os bancos de dados relacionados estão presentes (o que retornará o erro JET_errAttachedDatabaseMismatch em circunstâncias normais) e o cliente quiser que a recuperação continue apesar dos bancos de dados ausentes, o erro JET_bitReplayIgnoreMissingDB será usado para continuar a recuperação para os bancos de dados disponíveis.

Como a recuperação de falha geralmente não acontece no mesmo computador (e com a mesma configuração) que no momento da falha, um banco de dados normalmente não altera o local. Em determinados cenários, como a movimentação de arquivos para um computador diferente ou a restauração de backup de instantâneo em locais diferentes, isso não é mais verdadeiro. A função **JetInit3** permite que você especifique um mapeamento (usando as estruturas [JET_RSTINFO](./jet-rstinfo-structure.md) e [JET_RSTMAP](./jet-rstmap-structure.md) ) entre o local do banco de dados antigo e seu novo local. Na verdade, você precisa apenas do novo local, desde que os arquivos de banco de dados estejam presentes nesse local. Assim que você souber os locais dos bancos de dados restaurados, a assinatura do banco de dados será usada para identificar o banco de dados por meio do processo de restauração. Você precisará do local do banco de dados original somente se precisar recriar um banco de dados, caso em que a assinatura é conhecida.

Além disso, se você precisar interromper uma recuperação após uma operação de desfazer, poderá especificar uma posição de log específica na qual a recuperação será interrompida. Observe que isso inclui a capacidade de parar no final de uma geração de log específica se a posição especificada fizer parte da geração, mas após o final do log real.

Para obter mais informações, consulte a seção "Comentários" no tópico [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Cliente</p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p>parâmetro</p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Usa ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Implementado como <strong>JetInit3W</strong> (Unicode) e <strong>JetInit3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do recurso](./resource-parameters.md)
