---
description: 'Saiba mais sobre: Função JetGetBookmark'
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
ms.openlocfilehash: ba7074ee7dff938f215e261a95f0f4b11f257cab0fa0469347a2413643e0bcf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889606"
---
# <a name="jetgetbookmark-function"></a>Função JetGetBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetbookmark-function"></a>Função JetGetBookmark

A **função JetGetBookmark** recupera o indicador do registro associado à entrada de índice na posição atual de um cursor. Esse indicador pode ser usado para reposicionar esse cursor de volta para o mesmo registro usando [JetGoToBookmark](./jetgotobookmark-function.md).

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

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvBookmark*

O buffer de saída que recebe o indicador.

*cbMax*

O tamanho máximo, em bytes, do buffer de saída.

*pcbActual*

O tamanho real, em bytes, do indicador.

Se esse parâmetro for **NULL,** o tamanho real do indicador não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real do indicador ainda será retornado. Isso significa que esse número será maior que o tamanho do buffer de saída.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber todo o indicador. O buffer de saída foi preenchido com o máximo de indicadores que caberia. O tamanho real do indicador também foi retornado, se solicitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong> Esses valores de retorno são introduzidos Windows XP.</p></td>
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
<p><strong>Windows XP:</strong> Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem-sucedida, o indicador do registro associado à entrada de índice na posição atual de um cursor será retornado no buffer de saída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado do buffer de saída e o tamanho real do indicador serão indefinido, a menos que JET_errBufferTooSmall tenha sido retornado. No caso de JET_errBufferTooSmall retornado, o buffer de saída conterá a maior parte do indicador que se ajustará ao espaço fornecido e o tamanho real do indicador será preciso. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Os indicadores geralmente devem ser tratados como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes condições são verdadeiras para todos os indicadores ESENT:

  - Um indicador identifica exclusivamente um registro em uma determinada tabela.

  - O indicador de um registro não será altere durante o tempo de vida desse registro.

  - O indicador de um registro é o mesmo que a chave desse registro no índice primário sobre a tabela que contém esse registro. Se nenhum índice primário for definido sobre essa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.

  - Indicadores podem ser comparados uns com os outros usando a [função memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário sobre a tabela dos registros de origem. Se nenhum índice primário for definido sobre essa tabela, não será significativo usar a ordenação relativa de indicadores dessa tabela.

  - Não faz sentido comparar indicadores de registros de tabelas diferentes entre si.

  - Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento, antes Windows Vista.
    
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
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
