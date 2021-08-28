---
description: 'Saiba mais sobre: função JetStopBackup'
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
ms.openlocfilehash: cd11857be7096ce30f2fcf06f8ab4f975185da57
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982359"
---
# <a name="jetstopbackup-function"></a>Função JetStopBackup


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetstopbackup-function"></a>Função JetStopBackup

A função **JetStopBackup** impede que qualquer atividade relacionada ao backup de streaming continue em uma instância em execução específica, encerrando assim o backup de streaming de forma previsível.

**Windows XP:**  essa função é introduzida no Windows XP.

[JetStopService](./jetstopservice-function.md) é a chamada herdada quando apenas uma instância é permitida. Nesse caso, a única instância ativa é aquela que está sendo preparada para encerramento.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Não está claro qual instância deve ser preparada para encerramento ao usar <a href="gg269240(v=exchg.10).md">JetStopService</a> com o modo de várias instâncias.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 



Se essa função for realizada com êxito, a instância começará a falhar quaisquer novas APIs de backup de streaming.

Se essa função falhar, nenhuma etapa a ser preparada para o término do backup na instância será executada e nenhuma alteração no estado da instância ocorrerá.

#### <a name="remarks"></a>Comentários

O backup é geralmente disparado por um evento fora do mecanismo de processo e usando essa API, o aplicativo ESENT em si fará outras chamadas para que as APIs de backup de streaming falhem. A maioria das APIs de backup de streaming começará a falhar com JET_errBackupAbortByServer. Assim, qualquer progresso de backup de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) retornará um erro. Operações de backup que fazem parte do encerramento de backup (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ainda serão permitidas.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
