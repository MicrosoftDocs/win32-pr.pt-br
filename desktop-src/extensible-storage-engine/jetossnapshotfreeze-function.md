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
ms.openlocfilehash: 854e38f91b894b1f7cc486a15afcfe857aaa31d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473962"
---
# <a name="jetossnapshotfreeze-function"></a>Função JetOSSnapshotFreeze


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotfreeze-function"></a>Função JetOSSnapshotFreeze

A função **JetOSSnapshotFreeze** inicia um instantâneo. Enquanto o instantâneo está em andamento, nenhuma atividade de gravação em disco pelo mecanismo pode ocorrer.

**Windows xp:** o **JetOSSnapshotFreeze** é introduzido no Windows XP.  

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Os ponteiros fornecidos para os parâmetros de saída são nulos, a sessão de instantâneo é inválida ou o parâmetro <em>grbit</em> é inválido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>A sessão de instantâneo não está no estado apropriado para iniciar um congelamento (por exemplo, um congelamento anterior falhou nesta sessão antes).</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>O mecanismo não está em um estado no qual um instantâneo pode ser executado. Um ou mais backups de streaming já estão em andamento ou uma ou mais instâncias estão passando por etapas de recuperação ou terminando.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A função falhou devido a uma condição de memória insuficiente.</p> | 
| <p>JET_errOutOfThreads</p> | <p>A função falhou porque um novo thread que está fazendo a congelamento falhou ao iniciar.</p> | 



Se essa função for realizada com sucesso, não haverá nenhum IOs de gravação emitido para os arquivos de banco de dados ou para os arquivos de log que fazem parte das instâncias que estão congeladas. Além disso, as informações da instância serão preenchidas corretamente e deverão ser liberadas posteriormente chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.

Se essa função falhar, o mecanismo continuará funcionando normalmente com o IOs ocorrendo como de costume. Não é necessário chamar [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) se a congelamento falhar. Além disso, as informações da instância não serão preenchidas, portanto, não é necessário liberar esse recurso.

#### <a name="remarks"></a>Comentários

Durante o período de congelamento, não haverá nenhum IOs de gravação emitido para os bancos de dados anexados ou os logs de transações, embora possa haver um IOs de gravação emitido para os bancos de dados temporários ou arquivos de streaming.

O estado no qual os bancos de dados e os arquivos de log estarão durante o congelamento (o estado em que os arquivos estaria em uma imagem de instantâneo de volume) será de forma que uma recuperação normal seja possível se esses arquivos forem restaurados posteriormente.

Como não há nenhuma operação de gravação durante o período de congelamento, as chamadas de API normais no mecanismo podem ser interrompidas para esse intervalo. O aplicativo cliente deve ser capaz de lidar com chamadas de API que podem demorar mais tempo normal se um congelamento ocorrer.

Devido aos possíveis efeitos descritos acima, há um tempo limite interno após o qual a sessão de instantâneo interromperá a fase congelar, mesmo que as APIs que fazem a descongelação ou anulação não tenham sido chamadas. O valor do tempo limite pode ser alterado usando o parâmetro do sistema [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) . Observe que o intervalo de congelamento típico está no intervalo de 10 segundos com o tempo limite padrão em cerca de 60 segundos.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
