---
description: 'Saiba mais sobre: função JetGetBookmark'
title: Função JetGetBookmark
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091777"
---
# <a name="jetgetbookmark-function"></a>Função JetGetBookmark


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>Função JetGetBookmark

A função **JetGetBookmark** recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando [JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvBookmark*

O buffer de saída que recebe o indicador.

*cbMax*

O tamanho máximo, em bytes, do buffer de saída.

*pcbActual*

O tamanho real, em bytes, do indicador.

Se esse parâmetro for **nulo** , o tamanho real do indicador não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real do indicador ainda será retornado. Isso significa que esse número será maior do que o tamanho do buffer de saída.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber o indicador inteiro. O buffer de saída foi preenchido com a maior parte do indicador que couber. O tamanho real do indicador também foi retornado, se solicitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:  </strong> Esses valores de retorno são apresentados no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado após o último registro no índice atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, o indicador do registro associado à entrada de índice na posição atual de um cursor será retornado no buffer de saída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado do buffer de saída e o tamanho real do indicador serão indefinidos, a menos que JET_errBufferTooSmall seja retornado. No caso em que JET_errBufferTooSmall for retornado, o buffer de saída conterá a maior parte do indicador que se ajustará no espaço fornecido e o tamanho real do indicador será preciso. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Os indicadores geralmente devem ser tratados como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes condições são verdadeiras de todos os indicadores de ESENT:

  - Um indicador identifica exclusivamente um registro em uma determinada tabela.

  - O indicador de um registro não será alterado durante o tempo de vida desse registro.

  - O indicador de um registro é o mesmo que a chave desse registro no índice primário na tabela que contém esse registro. Se nenhum índice primário for definido nessa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.

  - Os indicadores podem ser comparados entre si usando a função [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário na tabela dos registros de origem. Se nenhum índice primário for definido nessa tabela, não será significativo usar a ordenação relativa de indicadores dessa tabela.

  - Não há sentido comparar indicadores de registros de tabelas diferentes entre si.

  - Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento, antes do Windows Vista.
    
**Windows Vista:** No Windows Vista e versões posteriores, os indicadores podem ser maiores que JET_cbBookmarkMost (256) bytes. O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
