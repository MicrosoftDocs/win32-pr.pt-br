---
description: 'Saiba mais sobre: Função JetGotoSecondaryIndexBookmark'
title: Função JetGotoSecondaryIndexBookmark
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e720286c3e7308078d5d5ec91aa27edc95b725830824473e7b5858f2de5bc90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072474"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Função JetGotoSecondaryIndexBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgotosecondaryindexbookmark-function"></a>Função JetGotoSecondaryIndexBookmark

A **função JetGotoSecondaryIndexBookmark** posiciona um cursor para uma entrada de índice associada ao indicador de índice secundário especificado. O indicador de índice secundário deve ser usado com o mesmo índice na mesma tabela da qual foi originalmente recuperado. O indicador de índice secundário para uma entrada de índice pode ser recuperado usando **JetGotoSecondaryIndexBookmark**.

**Windows XP:****JetGotoSecondaryIndexBookmark** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvSecondaryKey*

O buffer que contém a chave secundária a ser usada para posicionar o cursor.

*cbSecondaryKey*

O tamanho da chave secundária no buffer.

*pvPrimaryBookmark*

O buffer que contém o indicador de chave primária a ser usado para posicionar o cursor.

*cbPrimaryBookmark*

O tamanho do indicador de chave primária no buffer.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>Caso a entrada de índice não possa mais ser encontrada, o cursor será posicionado à esquerda onde essa entrada de índice foi encontrada anteriormente. A operação ainda falhará com JET_errRecordDeleted; no entanto, será possível mover para a entrada de índice seguinte ou anterior em relação à entrada de índice que agora está ausente.</p></td>
</tr>
</tbody>
</table>


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
<td><p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque é porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>O indicador de índice secundário fornecido era inválido. Esse erro pode ter ocorrido porque a chave secundária é zero ou o ponteiro do buffer de chave secundária é <strong>NULL.</strong> Esse erro ocorre porque</p>
<ul>
<li><p>O índice secundário atual não tem uma restrição de exclusividade e o tamanho do indicador fornecido é zero.</p></li>
<li><p>O ponteiro do buffer de indicador é <strong>NULL.</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>O cursor não está atualmente em um índice secundário. Não é significativo ir para um indicador de índice secundário quando o cursor não está usando um índice secundário no momento. <a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> deve ser usado quando o cursor não está em um índice secundário.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Não foi possível encontrar a entrada de índice associada ao indicador de índice secundário.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem-sucedida, o cursor será posicionado em uma entrada de índice associada ao indicador de índice secundário especificado. Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor usar, essa chave de pesquisa será excluída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, a posição do cursor permanecerá inalterada, a menos que JET_errRecordDeleted seja retornado e JET_bitBookmarkPermitVirtualCurrency for especificado. Nesse caso, o cursor será posicionado onde a entrada de índice associada ao indicador de índice secundário especificado teria sido. O cursor pode ser movido em relação a essa posição, mas ainda não está em uma entrada de índice válida.

Se um registro tiver sido preparado para atualização, essa atualização será cancelada. Se um intervalo de índice estiver em vigor, esse intervalo de índice será cancelado. Se uma chave de pesquisa tiver sido construída para o cursor usar, essa chave de pesquisa será excluída. Em qualquer caso, nenhuma alteração no estado do banco de dados ocorrerá.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
