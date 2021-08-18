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
ms.openlocfilehash: a13415d8174a48e7e9f33d1459ca9a0a07271421101e65236f8f03263ea2a898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849656"
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

Para criar essa máscara de bit, basta ou em conjunto motivos válidos de retorno de chamada [da enumeração JET_CBTYP](./jet-cbtyp.md) de bits.

*pCallback*

O ponteiro de função para a função de retorno de chamada para o aplicativo.

*pvContext*

Especifica um ponteiro de contexto que será dado à função de retorno de chamada para o aplicativo.

*phCallbackId*

Retorna um alça que pode ser usado posteriormente para cancelar o registro da função de retorno de chamada determinada usando [JetUnregisterCallback](./jetunregistercallback-function.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Esse erro será retornado por <strong>JetRegisterCallback</strong> quando:</p>
<ul>
<li><p><em>cbtyp</em> é zero,</p></li>
<li><p><em>pCallback</em> é NULL.</p></li>
<li><p><em>phCallbackId</em> é NULL.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, o retorno de chamada especificado será registrado pelos motivos de retorno de chamada especificados com a tabela associada ao cursor especificado. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o retorno de chamada não será registrado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Esse método fornece um meio para o aplicativo associar retornos de chamada voláteis a uma tabela em um banco de dados. Se o aplicativo quiser associar retornos de chamada persistentes a uma tabela no banco de dados, ele deverá passar o retorno de chamada para JET_TABLECREATE [usando](./jet-tablecreate-structure.md) [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
