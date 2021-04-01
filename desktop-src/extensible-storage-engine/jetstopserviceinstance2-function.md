---
description: 'Saiba mais sobre: função JetStopServiceInstance2'
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
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647344"
---
# <a name="jetstopserviceinstance2-function"></a>Função JetStopServiceInstance2


_**Aplica-se a:** Windows | Windows Server_

A função **JetStopServiceInstance2** prepara uma instância antes da suspensão e prepara uma instância após a retomada. Suspender e retomar são Estados de execução do modelo de ciclo de vida do aplicativo da Windows Store.

A função **JetStopServiceInstance2** foi introduzida no Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância de destino. O tipo de dados **JET_INSTANCE** é um identificador para a instância do banco de dado a ser usado para uma chamada para a API do Jet. Esse identificador é obtido quando você cria uma instância do banco de dados chamando as funções [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .

*grbit*

Um grupo de bits que especifica um ou mais dos valores listados e definidos na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Interrompe todos os serviços ESE (mecanismo de armazenamento extensível) para a instância especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Interrompe tarefas de manutenção em segundo plano especificadas pelo cliente reiniciáveis (desfragmentação da árvore B +, por exemplo).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Quiesces todos os caches sujos em disco. Esse valor é assíncrono e pode ser cancelado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Retoma as operações StopService emitidas anteriormente; ou seja, ele reinicia o serviço. Esse valor pode ser combinado com o parâmetro <em>grbits</em> para retomar serviços específicos ou com JET_bitStopServiceAll para retomar todos os serviços interrompidos anteriormente. Esse bit só pode ser usado para retomar StopServiceBackgroundUserTasks e JET_bitStopServiceQuiesceCaches. Se você tiver chamado anteriormente com JET_bitStopServiceAll, uma tentativa de usar JET_bitStopServiceResume falhará. Se a segunda etapa de retomada não for chamada, o aplicativo causará degradação do desempenho. Nessa situação, o ponto de verificação é mantido em zero.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Retornar valor

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
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Essa função permite que um aplicativo JET mova o cache do banco de dados para um estado limpo ou quase limpo (com o sistema operacional ocioso de e/s), de modo que, se o aplicativo fosse encerrado, a recuperação seria rápida. Essa abordagem é preferida sobre o JET de terminação chamando as funções [JetTerm](./jetterm-function.md) ou [JetDetachDatabase](./jetdetachdatabase-function.md) , de modo que, no cenário mais comum, o aplicativo seja simplesmente dessuspenso e, posteriormente, o aplicativo tenha todo o cache e esteja pronto para ser o mais rápido possível.

Se essa função for realizada com sucesso, ela prepara o cache do banco de dados para uma suspensão iminente. Essa função enfileira trabalhos em um thread de trabalho em segundo plano e retorna ao chamador imediatamente. A função deve ser chamada com base no VisibilityNotice de PLM em vez de chamar do manipulador de eventos de suspensão do aplicativo para garantir que o JET tenha tempo para liberar buffers sujos antes de o PLM suspender/encerrar o processo. Internamente, o JET dispara um despacho imediato da manutenção do ponto de verificação após a alteração da configuração (ou seja, a atualização do ponto de verificação ou esse novo bit de cache). Para obter mais informações sobre eventos VisibilityNotice, consulte [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Essa função deve ser chamada duas vezes. Ele é chamado depois que o aplicativo recebe o aviso de suspensão do sistema operacional, mas antes de o aplicativo ser suspenso. Em seguida, ele é chamado novamente depois que o sistema operacional retoma o aplicativo. Por exemplo:

Quando chamado para suspender: JET_ERR JET_API JetStopServiceInstance2 (instância, JET_bitStopServiceQuiesceCaches);

Quando retomado: JET_ERR JET_API JetStopServiceInstance2 (instância, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Confira também

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
