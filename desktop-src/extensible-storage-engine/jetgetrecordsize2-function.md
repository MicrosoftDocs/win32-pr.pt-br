---
description: 'Saiba mais sobre: função JetGetRecordSize2'
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
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787668"
---
# <a name="jetgetrecordsize2-function"></a>Função JetGetRecordSize2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetrecordsize2-function"></a>Função JetGetRecordSize2

A função **JetGetRecordSize2** recupera informações de tamanho de registro do local desejado.

**Windows 7: o JetGetRecordSize2** é introduzido no sistema operacional Windows 7.

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

Identifica o contexto de sessão de banco de dados que será usado para a chamada à API.

*TableID*

Identifica a tabela ou o cursor que será usado para a chamada à API. O cursor deve ser posicionado em um registro ou ter uma atualização preparada.

*precsize*

Um ponteiro para um buffer de saída para a estrutura de [JET_RECSIZE2](./jet-recsize2-structure.md) .

*grbit*

Este é um ou mais dos valores a seguir.

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Isso recupera o tamanho do registro que está no buffer de cópia preparado para atualização. Caso contrário, o <em>TableName</em> ou o cursor deve ser posicionado em um registro e esse registro será usado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Quando esse bit é especificado, o <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> não é zerado antes de preencher o conteúdo, agindo efetivamente como um acúmulo das estatísticas de vários registros visitados ou atualizados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>Isso faz com que a API ignore valores longos não intrínsecos. Por exemplo, somente o registro local na página será usado.</p></td>
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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Uma das opções solicitadas era inválida ou não foi implementada. Esse erro será retornado pela função <strong>JetGetRecordSize2</strong> quando um <em>grbit</em> ilegal for especificado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable só será retornada pelo sistema operacional Windows XP e pelas versões posteriores do Windows.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>É ilegal usar a mesma sessão para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable será retornado somente pelo Windows XP e por versões posteriores do Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Isso pode acontecer se o cursor foi posicionado incorretamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Se o cursor não tiver sido posicionado em uma transação, isso poderá acontecer se outro thread excluir o registro de fora desta sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Isso pode ser retornado se um <strong></strong><em>precsize</em> nulo foi passado.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

O tamanho da chave acumulada no campo **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md), é afetado pelo JET_bitRecordSizeInCopyBuffer. Se esse bit for especificado, o tamanho da chave acumulado no campo **cbOverhead** será o tamanho de chave completo. Se esse bit não for usado, o tamanho da chave acumulado não incluirá nenhum tamanho salvo devido à compactação de prefixo de chave.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
