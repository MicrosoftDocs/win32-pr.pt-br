---
description: 'Saiba mais sobre: função JetSetLS'
title: Função JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c24a0d1cf45d370482b4890451569900aac946e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465293"
---
# <a name="jetsetls-function"></a>Função JetSetLS


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetls-function"></a>Função JetSetLS

a função **JetSetLS** permite que o aplicativo associe um identificador de contexto conhecido como Local Armazenamento com um cursor ou a tabela associada a esse cursor. Esse identificador de contexto pode ser usado pelo aplicativo para armazenar dados auxiliares associados a um cursor ou tabela. O aplicativo é notificado posteriormente usando um retorno de chamada de tempo de execução quando o identificador de contexto deve ser liberado. Isso torna possível associar o estado alocado dinamicamente a um cursor ou tabela.

**Windows xp:** o **JetSetLS** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*ls*

O identificador de contexto a ser associado ao cursor ou à tabela.

Quando JET_bitLSReset for especificado, o valor real desse parâmetro será ignorado e JET_LSNil será usado.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>Essa opção indica que o identificador de contexto deve ser associado ao cursor fornecido.</p><p>Se nem JET_bitLSCursor nem JET_bitLSTable forem especificadas, JET_bitLSCursor será presumido.</p><p>É ilegal usar essa opção com JET_bitLSTable. A operação falhará com JET_errInvalidgrbit se for tentada.</p> | 
| <p>JET_bitLSReset</p> | <p>Essa opção indica que o identificador de contexto especificado deve ser ignorado e que o identificador de contexto para o objeto escolhido deve ser redefinido para JET_LSNil.</p><p>É importante observar que essa ação não resultará em um retorno de chamada para limpar o valor anterior do identificador de contexto para o objeto escolhido. A limpeza adequada do identificador de contexto anterior pode ser obtida usando <a href="gg269234(v=exchg.10).md">JetGetLS</a> com JET_bitLSReset. Consulte <a href="gg269234(v=exchg.10).md">JetGetLS</a> para obter mais informações.</p> | 
| <p>JET_bitLSTable</p> | <p>Essa opção indica que o identificador de contexto deve ser associado à tabela associada ao cursor fornecido.</p><p>É ilegal usar essa opção com JET_bitLSCursor. A operação falhará com JET_errInvalidgrbit se for tentada.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma das opções solicitadas era inválida, foi usada incorretamente ou não foi implementada. Isso pode ocorrer para <strong>JetSetLS</strong> quando JET_bitLSCursor e JET_bitLSTable são especificados.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errLSAlreadySet</p> | <p>O identificador de contexto fornecido não pôde ser associado ao objeto solicitado porque ele já tinha um identificador de contexto associado a ele.</p> | 
| <p>JET_errLSCallbackNotSpecified</p> | <p>O identificador de contexto fornecido não pôde ser associado ao objeto solicitado porque o retorno de chamada de tempo de execução não foi configurado para a instância associada à sessão.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, o identificador de contexto fornecido foi associado com êxito ao objeto solicitado. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, nenhuma alteração no estado do objeto solicitado ocorreu. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

o Armazenamento Local para um cursor ou uma tabela deve ser exibido como um cache volátil. O aplicativo deve primeiro tentar recuperar o identificador de contexto usando [JetGetLS](./jetgetls-function.md). Se o valor não for definido (ou seja, JET_LSNil), o aplicativo deverá criar um novo contexto e carregá-lo no cache usando **JetSetLS**. O aplicativo pode limpar o cache usando uma chamada para [JetGetLS](./jetgetls-function.md) com JET_bitLSReset. Se o mecanismo de banco de dados limpar o cache, um retorno de chamada de tempo de execução será gerado para dar ao aplicativo a oportunidade de limpar esse contexto. O tipo de retorno de chamada será JET_cbtypFreeCursorLS para um identificador de contexto associado a um cursor e JET_cbtypFreeTableLS para um identificador de contexto associado a uma tabela. Em ambos os casos, o identificador de contexto será passado como pvArg1. Consulte [JET_CALLBACK](./jet-callback-callback-function.md) para obter mais informações.

o retorno de chamada de tempo de execução deve ser configurado corretamente para a instância associada à sessão especificada antes que a Armazenamento Local possa ser usada. Esse retorno de chamada pode ser definido usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramRuntimeCallback](./callback-parameters.md). Consulte [JetSetSystemParameter](./jetsetsystemparameter-function.md) e [JET_paramRuntimeCallback](./callback-parameters.md) em parâmetros do sistema para obter mais informações.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
