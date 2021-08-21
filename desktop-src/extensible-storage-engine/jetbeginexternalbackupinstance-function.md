---
description: 'Saiba mais sobre: função JetBeginExternalBackupInstance'
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
ms.openlocfilehash: 55fc5a204ce321f0be5073f2c4c9ab2a80a11a822b3bf23c87441770c3a1857b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118073014"
---
# <a name="jetbeginexternalbackupinstance-function"></a>Função JetBeginExternalBackupInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbeginexternalbackupinstance-function"></a>Função JetBeginExternalBackupInstance

A função **JetBeginExternalBackupInstance** inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.

**Windows xp: o JetBeginExternalBackupInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância do banco de dados a ser usada para esta chamada.

para Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global é implícito nesse caso.

para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade Windows 2000) em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Esse sinalizador foi preterido. O uso desse bit resultará na JET_errInvalidgrbit retornando.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro. definido para Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

O sistema pode gerar códigos de êxito ou de falha como resultado de uma chamada para essa função. para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de Armazenamento extensível](./extensible-storage-engine-error-codes.md).

Consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Comentários

**JetBeginExternalBackupInstance** é a primeira função em uma série de funções que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito. Consulte também [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) e [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Um backup externo pode ser usado para implementar backups completos, incrementais ou diferenciais.

O backup será difuso, pois o backup será consistente para um único ponto no histórico de transações, mas controlar o ponto exato no tempo não é possível no momento.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p></td>
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
