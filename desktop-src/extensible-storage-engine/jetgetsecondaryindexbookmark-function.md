---
description: 'Saiba mais sobre: função JetGetSecondaryIndexBookmark'
title: Função JetGetSecondaryIndexBookmark
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787667"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>Função JetGetSecondaryIndexBookmark


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetsecondaryindexbookmark-function"></a>Função JetGetSecondaryIndexBookmark

A função **JetGetSecondaryIndexBookmark** recupera um indicador especial para a entrada de índice secundário na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar com eficiência esse cursor de volta para a mesma entrada de índice usando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Isso é mais útil ao reposicionar em um índice secundário que contém chaves duplicadas ou que contém várias entradas de índice para o mesmo registro.

**Windows XP: o JetGetSecondaryIndexBookmark** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvSecondaryKey*

O buffer de saída que recebe a chave secundária.

*cbSecondaryKeyMax*

O tamanho máximo, em bytes, do buffer de saída para a chave secundária.

*pcbSecondaryKeyActual*

Recebe o tamanho real em bytes da chave secundária.

Se esse parâmetro for NULL, o tamanho real da chave secundária não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real da chave secundária ainda será retornado. Isso significa que esse número será maior do que o tamanho do buffer de saída.

*pvPrimaryBookmark*

O buffer de saída que recebe o indicador de chave primária.

*cbPrimaryBookmarkMax*

O tamanho máximo, em bytes, do buffer de saída para o indicador de chave primária.

*pcbPrimaryKeyActual*

Recebe o tamanho real, em bytes, do indicador de chave primária.

Se esse parâmetro for NULL, o tamanho real do indicador de chave primária não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real do indicador de chave primária ainda será retornado. Isso significa que esse número será maior do que o tamanho do buffer de saída.

*grbit*

Reservado para uso futuro.

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
<td><p>A operação foi concluída com êxito, mas um dos buffers de saída era muito pequeno para receber os dados solicitados.</p>
<p>O buffer de saída foi preenchido com a maior parte do indicador que couber. O tamanho real do indicador também foi retornado, se solicitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>O cursor não está em um índice secundário no momento.</p>
<p>Não é significativo recuperar um indicador de índice secundário quando o cursor não está usando um índice secundário no momento. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve ser usado quando o cursor não estiver em um índice secundário.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro.</p>
<p>Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p></td>
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
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o indicador de índice secundário para a entrada de índice na posição atual de um cursor será retornado nos buffers de saída. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado dos buffers de saída e o tamanho real do indicador de índice secundário serão indefinidos, a menos que JET_errBufferTooSmall seja retornado. No caso em que JET_errBufferTooSmall for retornado, os buffers de saída conterão a maior parte do indicador de índice secundário que se ajustará no espaço fornecido e o tamanho real do indicador de índice secundário será preciso. De qualquer forma, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Os indicadores geralmente devem ser tratados como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes propriedades podem ser conhecidas sobre todos os indicadores de ESENT:

  - Um indicador identifica exclusivamente um registro em uma determinada tabela.

  - O indicador de um registro não será alterado durante o tempo de vida desse registro.

  - O indicador de um registro é o mesmo que a chave desse registro no índice primário na tabela que contém esse registro. Se nenhum índice primário for definido nessa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.

  - Os indicadores podem ser comparados entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário na tabela dos registros de origem. Se nenhum índice primário for definido nessa tabela, a ordenação relativa de indicadores dessa tabela não será significativa.

  - Não há sentido comparar indicadores de registros de tabelas diferentes entre si.

  - Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento antes do Windows Vista. No Windows Vista e versões posteriores, os indicadores podem ser maiores. O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.

As chaves devem ser geralmente tratadas como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes propriedades podem ser conhecidas sobre todas as chaves ESENT:

  - As chaves podem ser comparadas entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice de origem sobre a tabela das entradas de índice de origem.

  - Não há sentido para comparar chaves de entradas de índice de índices diferentes entre si.

  - Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes do Windows Vista. No Windows Vista e versões posteriores, as chaves podem ser maiores. O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.

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
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
