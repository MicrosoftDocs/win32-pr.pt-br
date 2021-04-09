---
description: 'Saiba mais sobre: função JetRetrieveKey'
title: Função JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011703"
---
# <a name="jetretrievekey-function"></a>Função JetRetrieveKey


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>Função JetRetrieveKey

A função **JetRetrieveKey** recupera a chave da entrada de índice na posição atual de um cursor. Essas chaves são construídas por chamadas para [JetMakeKey](./jetmakekey-function.md). A chave recuperada pode então ser usada para retornar com eficiência esse cursor para a mesma entrada de índice por uma chamada para [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvData*

O buffer de saída que receberá a chave.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Recebe o tamanho real em bytes da chave.

Se esse parâmetro for nulo, o tamanho real da chave não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real da chave ainda será retornado. Isso significa que esse número será maior do que o tamanho do buffer de saída.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Quando especificado, o mecanismo retornará a chave de pesquisa para o cursor. A chave de pesquisa é criada usando uma ou mais chamadas anteriores para <a href="gg269329(v=exchg.10).md">JetMakeKey</a> para fins de busca dessa chave usando <a href="gg294103(v=exchg.10).md">JetSeek</a> ou definindo um intervalo de índice usando <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p></td>
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
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Não há uma chave de pesquisa atual para o cursor. Isso ocorrerá para <strong>JetRetrieveKey</strong> se JET_bitRetrieveCopy for especificado e uma chave de pesquisa não tiver sido construída para este cursor usando uma chamada anterior para <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. A chave de pesquisa será excluída por uma chamada anterior para qualquer API de navegação no cursor que não seja <a href="gg294117(v=exchg.10).md">JetMove</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p></td>
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
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber a chave inteira. O buffer de saída foi preenchido com o máximo de chave que se ajustaria. O tamanho real da chave também foi retornado, se solicitado.</p>
<p><strong>Observação</strong>   Esse erro não será retornado se JET_bitRetrieveCopy for especificado. Consulte a seção comentários para obter mais informações.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a chave para a entrada de índice na posição atual de um cursor será retornada no buffer de saída. Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá a maior parte da chave que se ajustará no espaço fornecido e o tamanho real da chave será preciso. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado do buffer de saída e o tamanho real da chave serão indefinidos. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

As chaves devem ser geralmente tratadas como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes propriedades podem ser conhecidas sobre todas as chaves ESENT:

  - As chaves podem ser comparadas entre si usando a função [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para estabelecer sua ordenação relativa no índice de origem sobre a tabela das entradas de índice de origem.

  - Não há sentido para comparar chaves de entradas de índice de índices diferentes entre si.

  - Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes do Windows Vista. No Windows Vista e versões posteriores, as chaves podem ser maiores. O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.

Além das propriedades acima das chaves ESENT em geral, é importante observar que uma chave de pesquisa é diferente da chave para uma entrada de índice. Especificamente, uma chave de pesquisa pode ser maior que uma chave comum. Esse comprimento extra ocorre quando uma opção curinga é usada ao construir a chave de pesquisa. Consulte [JetMakeKey](./jetmakekey-function.md) para obter mais informações.

Há um bug importante nessa API que está presente em todas as versões. Se a chave de pesquisa for solicitada usando o uso de JET_bitRetrieveCopy e o buffer de saída for muito pequeno para receber a chave inteira, JET_wrnBufferTruncated não será retornado. JET_errSuccess será retornado em seu lugar. É importante verificar se o tamanho real da chave, como retornado usando *pcbActual* , é menor ou igual ao tamanho do buffer de saída. Se o tamanho real for maior do que o tamanho do buffer de saída, o chamador de **JetRetrieveKey** deverá reagir como se JET_wrnBufferTruncated retornassem em vez disso.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
