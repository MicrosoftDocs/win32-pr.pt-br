---
description: 'Saiba mais sobre: função JetTerm2'
title: Função JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090655"
---
# <a name="jetterm2-function"></a>Função JetTerm2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetterm2-function"></a>Função JetTerm2

A função **JetTerm2** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).

**JetTerm2** também pode destruir uma instância não inicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **nulo**.

**Windows XP e versões posteriores:**  Este parâmetro está sobrecarregado. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos valores a seguir.

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
<td><p>JET_bitTermComplete</p></td>
<td><p>Solicita que a instância seja desligada corretamente. Qualquer trabalho de limpeza opcional que normalmente seria feito em segundo plano em tempo de execução é concluído imediatamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>Solicita que a instância seja desligada o mais rápido possível. Qualquer trabalho opcional que normalmente seria feito em segundo plano em tempo de execução é abandonado.</p>
<p><strong>Observação</strong>  Essa opção pode causar perda de espaço temporária ou permanente no banco de dados. Esse espaço perdido sempre pode ser recuperado por meio de uma desfragmentação offline do banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>Solicita que a instância seja desligada mesmo que atualmente haja um backup em andamento. Normalmente, um backup pendente faria com que o <a href="gg269298(v=exchg.10).md">JetTerm</a> falhasse com JET_errBackupInProgress. Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitTermAbrupt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>Solicita que a instância seja desligada com todos os bancos de dados anexados deixados em um estado sujo.</p>
<p>Windows 7: o JET_bitTermDirty é introduzido no Windows 7.</p></td>
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
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Esse erro será retornado por <a href="gg269298(v=exchg.10).md">JetTerm</a> quando o mecanismo estiver no modo de várias instâncias e quando <em>pinstance</em> se referir a uma instância inválida.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>A instância não pode ser desligada porque existem sessões com transações ativas para a instância especificada. Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, a instância especificada será desligada. O identificador de instância também será fechado e ficará indisponível para qualquer API que usa um identificador de instância. Todos os outros objetos associados à instância, como sessões, também serão fechados. O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.

Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterado. Caso contrário, a instância ainda será desligada conforme indicado para o caso de êxito. A diferença é que a instância precisará passar pela recuperação de pane quando for inicializada na próxima vez. O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária. Conceitualmente, essa falha de [JetTerm](./jetterm-function.md) não é diferente de uma falha de processo.

#### <a name="remarks"></a>Comentários

Consulte [JetTerm](./jetterm-function.md).

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

[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
