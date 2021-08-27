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
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469693"
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

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Não está claro qual instância se preparar para o encerramento ao usar <a href="gg269240(v=exchg.10).md">JetStopService</a> com o modo de várias instâncias.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 



Se essa função for bem-sucedida, a instância começará a falhar em qualquer nova APIs de backup de streaming.

Se essa função falhar, nenhuma etapa de preparação para a terminação de backup na instância será realizada e nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

O backup geralmente é disparado por um evento fora do mecanismo de processo e, usando essa API, o próprio aplicativo ESENT fará outras chamadas para as APIs de backup de streaming falharem. A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer. Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro. As operações de backup que fazem parte da terminação de backup (como [JetEndExternalBackupInstance)](./jetendexternalbackupinstance-function.md)ainda serão permitidas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
