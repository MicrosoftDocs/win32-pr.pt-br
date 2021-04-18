---
description: 'Saiba mais sobre: função JetGetLS'
title: Função JetGetLS
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766414"
---
# <a name="jetgetls-function"></a>Função JetGetLS


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetls-function"></a>Função JetGetLS

A função **JetGetLS** permite que o aplicativo recupere o identificador de contexto conhecido como armazenamento local que está associado a um cursor ou à tabela associada a esse cursor. Esse identificador de contexto deve ter sido definido anteriormente usando [JetSetLS](./jetsetls-function.md). **JetGetLS** também pode ser usado para buscar simultaneamente o identificador de contexto atual para um cursor ou uma tabela e redefinir esse identificador de contexto.

**Windows XP: o JetGetLS** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pls*

O buffer de saída que recebe o identificador de contexto atualmente associado ao cursor ou à tabela.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

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
<td><p>JET_bitLSCursor</p></td>
<td><p>Indica que o identificador de contexto associado ao cursor fornecido deve ser recuperado.</p>
<p>Se nem JET_bitLSCursor nem JET_bitLSTable forem especificadas, JET_bitLSCursor será presumido.</p>
<p>Esta opção não pode ser usada com JET_bitLSTable. A operação falhará com JET_errInvalidgrbit se for tentada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Indica que o identificador de contexto associado à tabela que contém o cursor fornecido deve ser recuperado. É ilegal usar essa opção com JET_bitLSCursor. A operação falhará com JET_errInvalidgrbit se for tentada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Indica que o identificador de contexto para o objeto escolhido deve ser redefinido para JET_LSNil. O valor atual do identificador de contexto é retornado no buffer de saída.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma das opções solicitadas era inválida, usada de maneira ilegal ou não implementada.</p>
<p>Isso pode ocorrer para <strong>JetGetLS</strong> quando JET_bitLSCursor e JET_bitLSTable são definidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>O identificador de contexto não pôde ser retornado porque nenhum identificador de contexto está associado no momento ao objeto solicitado.</p>
<p><strong>Observação  </strong> Esse erro não será retornado se JET_bitLSReset for especificado, mas nenhum identificador de contexto foi associado ao objeto solicitado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o identificador de contexto foi recuperado com êxito do objeto solicitado. Se JET_bitLSReset tiver sido especificado, esse identificador de contexto também foi removido com êxito do objeto. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, nenhuma alteração no estado do objeto solicitado ocorreu. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
