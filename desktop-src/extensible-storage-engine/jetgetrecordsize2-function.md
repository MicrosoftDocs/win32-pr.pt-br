---
description: 'Saiba mais sobre: Função JetGetRecordSize2'
title: Função JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68c503192f0be157a59e8e3b32c817231f35e25c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478292"
---
# <a name="jetgetrecordsize2-function"></a>Função JetGetRecordSize2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetrecordsize2-function"></a>Função JetGetRecordSize2

A **função JetGetRecordSize2** recupera informações de tamanho do registro do local desejado.

**Windows 7: JetGetRecordSize2** é introduzido no sistema operacional Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

Identifica o contexto de sessão do banco de dados que será usado para a chamada à API.

*Tableid*

Identifica a tabela ou cursor que será usado para a chamada à API. O cursor deve ser posicionado em um registro ou ter uma atualização preparada.

*pré-ize*

Um ponteiro para um buffer de saída para a [estrutura JET_RECSIZE2](./jet-recsize2-structure.md) dados.

*grbit*

Esse é um ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização. Caso contrário, <em>tableid</em> ou cursor deverá ser posicionado em um registro e esse registro será usado.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Quando esse bit é <a href="gg269174(v=exchg.10).md"></a> especificado, o JET_RECSIZE2 é zerado antes de preencher o conteúdo, atuando efetivamente como um acúmulo das estatísticas para vários registros visitados ou atualizados.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Isso faz com que a API ignore valores longos não intrínsecos. Por exemplo, somente o registro local na página será usado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Uma das opções solicitadas era inválida ou não implementada. Esse erro será retornado pela função <strong>JetGetRecordSize2</strong> quando um <em>grbit ilegal</em> for especificado.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable será retornado apenas pelo sistema operacional Windows XP e versões posteriores do Windows.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>É ilegal usar a mesma sessão para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong> JET_errInstanceUnavailable será retornado apenas pelo WINDOWS XP e versões posteriores do Windows.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Isso pode acontecer se o cursor foi posicionado incorretamente.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Se o cursor não estiver posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro dessa sessão.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Isso poderá ser retornado se um<em>pré-size</em> <strong>NULL</strong>tiver sido passado.</p> | 



#### <a name="remarks"></a>Comentários

O tamanho da chave acumulada no campo **cbOverhead** [de JET_RECSIZE2](./jet-recsize2-structure.md), é afetado por JET_bitRecordSizeInCopyBuffer. Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho total da chave. Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação do prefixo de chave.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
