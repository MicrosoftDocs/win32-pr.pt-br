---
description: 'Saiba mais sobre: Função JetStopServiceInstance2'
title: Função JetStopServiceInstance2
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b5446306bd4035c68f33db2966b1cfadd0b6d82
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987229"
---
# <a name="jetstopserviceinstance2-function"></a>Função JetStopServiceInstance2


_**Aplica-se a:** Windows | Windows Servidor_

A **função JetStopServiceInstance2** prepara uma instância antes de Suspender e prepara uma instância após Retomar. Suspender e retomar são estados de execução do modelo de ciclo de vida do aplicativo Windows Store.

A **função JetStopServiceInstance2** foi introduzida no Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância de destino. O **JET_INSTANCE** de dados é um identificador para a instância do banco de dados a ser usado para uma chamada à API jet. Esse handle é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2,](./jetcreateinstance2-function.md) [JetInit](./jetinit-function.md)ou [JetInit2.](./jetinit2-function.md)

*grbit*

Um grupo de bits que especifica um ou mais dos valores listados e definidos na tabela a seguir.


| <p>Valor</p> | <p>Descrição</p> | 
|--------------|--------------------|
| <p>JET_bitStopServiceAll</p> | <p>Interrompe todos os serviços ESE (Extensible Armazenamento Engine) para a instância especificada.</p> | 
| <p>JET_bitStopServiceBackgroundUserTasks</p> | <p>Interrompe tarefas de manutenção em segundo plano especificadas pelo cliente reiniciáveis (Desfragmentação de Árvore B+, por exemplo).</p> | 
| <p>JET_bitStopServiceQuiesceCaches</p> | <p>Acumula todos os caches sujos no disco. Esse valor é assíncrono e pode ser cancelado.</p> | 
| <p>JET_bitStopServiceResume</p> | <p>Retoma as operações StopService emitidas anteriormente; ou seja, ele reinicia o serviço. Esse valor pode ser combinado com o <em>parâmetro grbits</em> para retomar serviços específicos ou com JET_bitStopServiceAll para Retomar todos os serviços interrompidos anteriormente. Esse bit só pode ser usado para retomar StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches. Se você tiver chamado anteriormente com JET_bitStopServiceAll, uma tentativa de usar JET_bitStopServiceResume falhará. Se a segunda etapa de retomada não for chamada, o aplicativo terá o desempenho degradado. Nessa situação, o ponto de verificação é mantido em zero.</p> | 



### <a name="return-value"></a>Valor retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 



#### <a name="remarks"></a>Comentários

Essa função permite que um aplicativo JET mova o cache do banco de dados para um estado limpo ou quase limpo (com a E/S do sistema operacional ociosa), de modo que, se o aplicativo fosse encerrado, a recuperação seria rápida. Essa abordagem é preferencial em vez de encerrar o JET chamando as funções [JetTerm](./jetterm-function.md) ou [JetDetachDatabase,](./jetdetachdatabase-function.md) para que, no cenário mais comum, o aplicativo seja apenas não aberto e, posteriormente, o aplicativo tenha todo o cache e esteja pronto para começar assim que possível.

Se essa função for bem-sucedida, ela preparará o cache do banco de dados para uma suspensão iminente. Essas filas de função funcionam para um thread de trabalho em segundo plano e retornam ao chamador imediatamente. A função deve ser chamada com base na VisibilityNotice do PLM em vez de chamar do manipulador de eventos de suspensão do aplicativo para garantir que o JET tenha tempo para liberar buffers sujos antes que o PLM suspenda/finaliza o processo. Internamente, o JET dispara uma expedição imediata da manutenção do ponto de verificação após a alteração da configuração (atualização do ponto de verificação ou esse novo bit de caches de quiesce). Para obter mais informações sobre eventos VisibilityNotice, consulte [Classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Essa função deve ser chamada duas vezes. Ele é chamado depois que o aplicativo recebe o aviso de suspensão do sistema operacional, mas antes que o aplicativo seja suspenso. Em seguida, ele é chamado novamente depois que o sistema operacional retoma o aplicativo. Por exemplo:

Quando chamado para Suspender: JET_ERR JET_API JetStopServiceInstance2( instância, JET_bitStopServiceQuiesceCaches);

Quando retomado: JET_ERR JET_API JetStopServiceInstance2( instância, JET_bitStopServiceQuiesceCaches| JET_bitStopServiceResume );

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
