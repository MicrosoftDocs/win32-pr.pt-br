---
description: 'Saiba mais sobre: Função JetBeginExternalBackupInstance'
title: Função JetBeginExternalBackupInstance
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95d74873fabfe27bc9750f074cd656b17e04803e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988070"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Função JetBeginExternalBackupInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbeginexternalbackupinstance-function"></a>Função JetBeginExternalBackupInstance

A **função JetBeginExternalBackupInstance** inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.

**Windows XP: JetBeginExternalBackupInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância de banco de dados a ser usada para essa chamada.

Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só poderá ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Esse sinalizador foi preterido. O uso desse bit resultará no JET_errInvalidgrbit sendo retornado.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Cria um backup incremental em vez de um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental terão o backup feito.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Reservado para uso futuro. Definido para Windows XP.</p> | 



### <a name="return-value"></a>Valor Retornado

O sistema pode gerar códigos de êxito ou falha como resultado de uma chamada para essa função. Para ver uma lista completa de erros para essa API, consulte [Extensible Armazenamento de erro do mecanismo](./extensible-storage-engine-error-codes.md).

Consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Comentários

**JetBeginExternalBackupInstance** é a primeira função em uma série de funções que devem ser chamadas para executar um backup online bem-sucedido (não baseado em VSS). Consulte também [JetBeginExternalBackup e](./jetbeginexternalbackup-function.md) [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Um backup externo pode ser usado para implementar backups completos, incrementais ou diferenciais.

O backup será difuso, já que o backup será consistente com um único ponto no tempo no histórico de transações, mas controlar o ponto exato no tempo não é possível no momento.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
