---
description: 'Saiba mais sobre: função JetSetTableSequential'
title: Função JetSetTableSequential
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808334"
---
# <a name="jetsettablesequential-function"></a>Função JetSetTableSequential


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>Função JetSetTableSequential

A função **JetSetTableSequential** notifica o mecanismo de banco de dados de que o aplicativo está verificando todo o índice atual que contém um determinado cursor. Consequentemente, os métodos usados para acessar os dados do índice serão ajustados para tornar esse cenário o mais rápido possível.

**Windows XP:** o **JetSetTableSequential** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>Essa opção é usada para indexar na direção de encaminhamento.</p>
<p><strong>Windows 7:</strong>o<strong>JET_bitPrereadForward</strong> é introduzido no Windows 7.  </p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>Essa opção é usada para indexar na direção de retrocesso.</p>
<p><strong>Windows 7:</strong>o<strong>JET_bitPrereadBackward</strong> é introduzido no Windows 7.  </p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram desativadas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, o índice atual do cursor será otimizado para uma verificação sequencial de todo o índice. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, nenhuma alteração na configuração do cursor ocorrerá. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se o aplicativo precisar examinar com eficiência um subconjunto conhecido de um índice, uma otimização semelhante também será executada sempre que um intervalo de índice for estabelecido usando [JetSetIndexRange](./jetsetindexrange-function.md). Essa otimização só está disponível no Windows XP e versões posteriores.

Se o aplicativo precisar examinar com eficiência um subconjunto desconhecido de um índice, nenhuma ação deverá ser executada. O mecanismo pode detectar automaticamente o comportamento da verificação e buscará os dados antecipadamente. No entanto, esse comportamento não é tão agressivo.

Essa otimização tornará a verificação do índice primário eficiente e fará com que a verificação apenas dos dados de entrada de índice em um índice secundário seja eficiente. Ele não fará a verificação de um índice secundário enquanto recupera dados de registro eficientes. Isso ocorre porque o mecanismo não executa uma leitura antecipada nos dados do registro.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
