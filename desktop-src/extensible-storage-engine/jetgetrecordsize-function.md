---
description: 'Saiba mais sobre: função JetGetRecordSize'
title: Função JetGetRecordSize
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f42defeefa4d01648d34b971cce994fbebf8f0e8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481292"
---
# <a name="jetgetrecordsize-function"></a>Função JetGetRecordSize


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetrecordsize-function"></a>Função JetGetRecordSize

A função **JetGetRecordSize** recupera informações de tamanho de registro do local desejado.

**Windows vista: o JetGetRecordSize** é introduzido no Windows Vista.

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

Identifica o contexto de sessão de banco de dados que será usado para a chamada à API.

*TableID*

Identifica a tabela ou o cursor que será usado para a chamada à API. O cursor deve ser posicionado em um registro ou ter uma atualização preparada.

*precsize*

Um ponteiro para um buffer de saída para a estrutura de [JET_RECSIZE](./jet-recsize-structure.md) .

*grbit*

Este é um ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização. Caso contrário, o <em>TableName</em> ou o cursor deve ser posicionado em um registro e esse registro será usado.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Quando esse bit é especificado, o <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> não é zerado antes de preencher o conteúdo, agindo efetivamente como um acúmulo das estatísticas de vários registros visitados ou atualizados.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Isso faz com que a API ignore valores longos não intrínsecos. Por exemplo, somente o registro local na página será usado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Uma das opções solicitadas era inválida ou não foi implementada. Esse erro será retornado pela função <strong>JetGetRecordSize</strong> quando um <em>grbit</em> ilegal for especificado.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable será retornado somente pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable será retornado somente pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Isso pode acontecer se o cursor foi posicionado incorretamente.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Se o cursor não tiver sido posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro de fora desta sessão.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Isso pode ser retornado se um <strong></strong><em>precsize</em> nulo foi passado.</p> | 



#### <a name="remarks"></a>Comentários

O tamanho da chave acumulada no campo **cbOverhead** de [JET_RECSIZE](./jet-recsize-structure.md), é afetado pelo JET_bitRecordSizeInCopyBuffer. Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho de chave completo. Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação de prefixo de chave.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
