---
description: 'Saiba mais sobre: Função JetRegisterCallback'
title: Função JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ef90466b736facf5bd9fefee31c0449964d003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985799"
---
# <a name="jetregistercallback-function"></a>Função JetRegisterCallback


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetregistercallback-function"></a>Função JetRegisterCallback

A **função JetRegisterCallback** permite que o aplicativo configure o mecanismo de banco de dados para emitir notificações ao aplicativo para eventos específicos. Essas notificações são associadas a uma tabela específica e permanecem em vigor somente até que a instância que contém a tabela seja fechada usando [JetTerm](./jetterm-function.md).

**Windows XP: JetRegisterCallback** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*cbtyp*

Uma máscara de bits composta pelos motivos de retorno de chamada para os quais o aplicativo deseja receber notificações.

Para criar essa máscara de bits, basta ou em conjunto motivos válidos de retorno de chamada da [enumeração JET_CBTYP](./jet-cbtyp.md) bit.

*pCallback*

O ponteiro de função para a função de retorno de chamada para o aplicativo.

*pvContext*

Especifica um ponteiro de contexto que será dado à função de retorno de chamada para o aplicativo.

*phCallbackId*

Retorna um alça que pode ser usado posteriormente para cancelar o registro da função de retorno de chamada determinada usando [JetUnregisterCallback](./jetunregistercallback-function.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <strong>JetRegisterCallback</strong> quando:</p><ul><li><p><em>cbtyp</em> é zero,</p></li><li><p><em>pCallback</em> é NULL.</p></li><li><p><em>phCallbackId</em> é NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, o retorno de chamada especificado será registrado pelos motivos de retorno de chamada especificados com a tabela associada ao cursor especificado. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o retorno de chamada não será registrado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Esse método fornece um meio para o aplicativo associar retornos de chamada voláteis a uma tabela em um banco de dados. Se o aplicativo quiser associar retornos de chamada persistentes a uma tabela no banco de dados, ele deverá passar o retorno de chamada para JET_TABLECREATE [usando](./jet-tablecreate-structure.md) [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)
