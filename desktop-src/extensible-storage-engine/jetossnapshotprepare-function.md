---
description: 'Saiba mais sobre: função JetOSSnapshotPrepare'
title: Função JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752754"
---
# <a name="jetossnapshotprepare-function"></a>Função JetOSSnapshotPrepare


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>Função JetOSSnapshotPrepare

A função **JetOSSnapshotPrepare** começa a preparação para uma sessão de instantâneo. Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não emite nenhum IOs de gravação para o disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlada por um gravador de instantâneo).

**Windows XP:** o **JetOSSnapshotPrepare** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*psnapId*

O identificador da sessão de instantâneo a ser iniciada.

*grbit*

As opções para esta chamada. Esse parâmetro pode ter uma combinação dos valores a seguir.

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
<td><p>0</p></td>
<td><p>Instantâneo normal.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIncrementalSnapshot</p></td>
<td><p>Somente os arquivos de log serão criados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCopySnapshot</p></td>
<td><p>Um instantâneo de cópia (normal ou incremental) sem truncamento de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitContinueAfterThaw</p></td>
<td><p>A sessão de instantâneo ocorre após <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e exigirá uma chamada de função <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitExplicitPrepare</p></td>
<td><p>Nenhuma instância será preparada por padrão.</p>
<p><strong>Windows 7:</strong>  JET_bitExplicitPrepare é introduzido no Windows 7.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>O ponteiro da ID do instantâneo é nulo ou o parâmetro <em>grbit</em> é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Uma sessão de instantâneo já está em andamento e a operação não tem permissão para ter mais de uma sessão de instantâneo em um determinado momento.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, uma sessão de instantâneo será capaz de iniciar a qualquer momento com a fase de congelamento de e/s. O identificador da sessão será retornado e deverá ser usado nas chamadas subsequentes para a sessão de instantâneo.

As instâncias em execução do mecanismo agora serão consideradas parte da sessão de instantâneo.

**Windows Vista:**  Para especificar um subconjunto diferente de instâncias, o [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) pode ser chamado.

A chamada de sequência de API normal é: **JetOSSnapshotPrepare**, opcionalmente seguido por uma ou mais chamadas para [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Quando o congelamento é iniciado, ele pode ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada abruptamente com [JetOSSnapshotAbort](./jetossnapshotabort-function.md).

Se JET_bitContinueAfterThaw for especificado após [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), a sessão de instantâneo permanecerá (embora a e/s seja retomada). Isso permitirá uma verificação do instantâneo e, se necessário, habilitará o truncamento de log usando [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e exigirá uma chamada para [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="remarks"></a>Comentários

As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
