---
description: 'Saiba mais sobre: Função JetStopBackup'
title: Função JetStopBackup
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36b62df437cc7e7b81b699308c1b1d28d9a8ebdb09a352769ea44eb3b836d73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614776"
---
# <a name="jetstopbackup-function"></a>Função JetStopBackup


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetstopbackup-function"></a>Função JetStopBackup

A **função JetStopBackup** impede que qualquer atividade relacionada ao backup de streaming continue em uma instância em execução específica, encerrando assim o backup de streaming de maneira previsível.

**Windows XP:**  Essa função é introduzida no Windows XP.

[JetStopService](./jetstopservice-function.md) é a chamada herdado quando apenas uma instância é permitida. Nesse caso, a única instância ativa é aquela que está sendo preparada para o encerramento.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Não está claro qual instância se preparar para o encerramento ao usar <a href="gg269240(v=exchg.10).md">JetStopService</a> com o modo de várias instâncias.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem-sucedida, a instância começará a falhar em qualquer nova APIs de backup de streaming.

Se essa função falhar, nenhuma etapa de preparação para a terminação de backup na instância será realizada e nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

O backup geralmente é disparado por um evento fora do mecanismo de processo e, usando essa API, o próprio aplicativo ESENT fará outras chamadas para as APIs de backup de streaming falharem. A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer. Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro. As operações de backup que fazem parte da terminação de backup (como [JetEndExternalBackupInstance)](./jetendexternalbackupinstance-function.md)ainda serão permitidas.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
