---
description: 'Saiba mais sobre: função JetOSSnapshotFreeze'
title: Função JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170723"
---
# <a name="jetossnapshotfreeze-function"></a>Função JetOSSnapshotFreeze


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>Função JetOSSnapshotFreeze

A função **JetOSSnapshotFreeze** inicia um instantâneo. Enquanto o instantâneo está em andamento, nenhuma atividade de gravação em disco pelo mecanismo pode ocorrer.

**Windows XP:** o **JetOSSnapshotFreeze** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapid*

O identificador da sessão de instantâneo.

*pcInstanceInfo*

O número de instâncias em execução no momento no mecanismo que fazem parte da sessão de instantâneo.

*paInstanceInfo*

Uma matriz de estruturas, uma para cada instância em execução que faz parte da sessão de instantâneo, descrevendo a instância e os bancos de dados que fazem parte dela.

*grbit*

As opções para esta chamada. Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0.

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
<td><p>Os ponteiros fornecidos para os parâmetros de saída são nulos, a sessão de instantâneo é inválida ou o parâmetro <em>grbit</em> é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>A sessão de instantâneo não está no estado apropriado para iniciar um congelamento (por exemplo, um congelamento anterior falhou nesta sessão antes).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>O mecanismo não está em um estado no qual um instantâneo pode ser executado. Um ou mais backups de streaming já estão em andamento ou uma ou mais instâncias estão passando por etapas de recuperação ou terminando.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>O identificador da sessão de instantâneo não é válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A função falhou devido a uma condição de memória insuficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>A função falhou porque um novo thread que está fazendo a congelamento falhou ao iniciar.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, não haverá nenhum IOs de gravação emitido para os arquivos de banco de dados ou para os arquivos de log que fazem parte das instâncias que estão congeladas. Além disso, as informações da instância serão preenchidas corretamente e deverão ser liberadas posteriormente chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.

Se essa função falhar, o mecanismo continuará funcionando normalmente com o IOs ocorrendo como de costume. Não é necessário chamar [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) se a congelamento falhar. Além disso, as informações da instância não serão preenchidas, portanto, não é necessário liberar esse recurso.

#### <a name="remarks"></a>Comentários

Durante o período de congelamento, não haverá nenhum IOs de gravação emitido para os bancos de dados anexados ou os logs de transações, embora possa haver um IOs de gravação emitido para os bancos de dados temporários ou arquivos de streaming.

O estado no qual os bancos de dados e os arquivos de log estarão durante o congelamento (o estado em que os arquivos estaria em uma imagem de instantâneo de volume) será de forma que uma recuperação normal seja possível se esses arquivos forem restaurados posteriormente.

Como não há nenhuma operação de gravação durante o período de congelamento, as chamadas de API normais no mecanismo podem ser interrompidas para esse intervalo. O aplicativo cliente deve ser capaz de lidar com chamadas de API que podem demorar mais tempo normal se um congelamento ocorrer.

Devido aos possíveis efeitos descritos acima, há um tempo limite interno após o qual a sessão de instantâneo interromperá a fase congelar, mesmo que as APIs que fazem a descongelação ou anulação não tenham sido chamadas. O valor do tempo limite pode ser alterado usando o parâmetro do sistema [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Observe que o intervalo de congelamento típico está no intervalo de 10 segundos com o tempo limite padrão em cerca de 60 segundos.

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
<td><p>Implementado como <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
