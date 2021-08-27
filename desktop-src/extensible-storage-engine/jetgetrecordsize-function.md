---
description: 'Saiba mais sobre: Função JetGetRecordSize'
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
ms.openlocfilehash: 15a94f14962559a63c19c6dce97b1d6dc5a234fd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982389"
---
# <a name="jetgetrecordsize-function"></a>Função JetGetRecordSize


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetrecordsize-function"></a>Função JetGetRecordSize

A **função JetGetRecordSize** recupera informações de tamanho do registro do local desejado.

**Windows Vista: JetGetRecordSize** é introduzido no Windows Vista.

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

Identifica o contexto de sessão do banco de dados que será usado para a chamada à API.

*Tableid*

Identifica a tabela ou cursor que será usado para a chamada à API. O cursor deve ser posicionado em um registro ou ter uma atualização preparada.

*pré-ize*

Um ponteiro para um buffer de saída para a [estrutura JET_RECSIZE](./jet-recsize-structure.md) dados.

*grbit*

Esse é um ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização. Caso contrário, <em>tableid</em> ou cursor deverá ser posicionado em um registro e esse registro será usado.</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>Quando esse bit é <a href="gg294072(v=exchg.10).md"></a> especificado, o JET_RECSIZE é zerado antes de preencher o conteúdo, atuando efetivamente como um acúmulo das estatísticas para vários registros visitados ou atualizados.</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>Isso faz com que a API ignore valores longos não intrínsecos. Por exemplo, somente o registro local na página será usado.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Uma das opções solicitadas era inválida ou não implementada. Esse erro será retornado pela função <strong>JetGetRecordSize</strong> quando um <em>grbit ilegal</em> for especificado.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable serão retornados somente por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>É ilegal usar a mesma sessão de mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  JET_errInstanceUnavailable serão retornados somente por Windows XP e versões posteriores.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Isso pode acontecer se o cursor foi posicionado incorretamente.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Se o cursor não estiver posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro dessa sessão.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Isso poderá ser retornado se um<em>pré-size</em> <strong>NULL</strong>tiver sido passado.</p> | 



#### <a name="remarks"></a>Comentários

O tamanho da chave acumulada no campo **cbOverhead** [de JET_RECSIZE](./jet-recsize-structure.md), é afetado por JET_bitRecordSizeInCopyBuffer. Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho total da chave. Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação do prefixo de chave.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
