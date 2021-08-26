---
description: 'Saiba mais sobre: Função JetGetThreadStats'
title: Função JetGetThreadStats
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d71dfac37d6b61ef5a5715f1766ba0967af8c99b2114a54efc439212ca06c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016176"
---
# <a name="jetgetthreadstats-function"></a>Função JetGetThreadStats


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetthreadstats-function"></a>Função JetGetThreadStats

A **função JetGetThreadStats** recupera informações de desempenho do mecanismo de banco de dados para o thread atual. Várias chamadas podem ser usadas para coletar estatísticas que refletem a atividade do mecanismo de banco de dados nesse thread entre essas chamadas.

**Windows Vista:****JetGetThreadStats** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parâmetros

*pvResult*

O buffer de saída que recebe os dados de estatísticas de thread. O buffer contém uma estrutura [JET_THREADSTATS](./jet-threadstats-structure.md) após uma chamada bem-sucedida.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

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
<td><p>A operação falhou porque o buffer de saída fornecido era muito pequeno para conter os dados solicitados. A <strong>função JetGetThreadStats</strong> retornará esse erro quando o buffer de saída for muito pequeno para conter a menor versão da estrutura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> com suporte pelo mecanismo de banco de dados.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, o buffer de saída conterá [uma estrutura JET_THREADSTATS](./jet-threadstats-structure.md) que contém estatísticas do mecanismo de banco de dados para o thread atual.

Em caso de falha, o estado do buffer de saída é indefinido.

#### <a name="remarks"></a>Comentários

As informações fornecidas por duas chamadas consecutivas dessa API destinam-se a serem usadas para calcular as despesas de qualquer outra operação do mecanismo de banco de dados no thread atual. Em geral, isso é feito por meio da leitura de antes e depois da leitura das estatísticas e da subtração da contagem após da contagem anterior para obter a contagem líquida de operações executadas.

Por exemplo, um aplicativo pode chamar **JetGetThreadStats** uma vez para obter uma leitura inicial das estatísticas do thread atual. Em seguida, ele poderia chamar a [função JetMove](./jetmove-function.md) com o parâmetro *cRow* definido como JET_MoveNext para passar para a próxima entrada de índice em um índice. Em seguida, ele **pode chamar JetGetThreadStats** novamente para obter outra leitura das estatísticas do thread. Em seguida, ele pode subtrair o contador cPageReferenced da segunda leitura da primeira. O resultado seria o número de páginas de banco de dados referenciadas pelo mecanismo de banco de dados para executar a [operação JetMove.](./jetmove-function.md)

As estatísticas de cada thread são acumuladas durante o tempo de vida desse thread. As estatísticas serão redefinidas se a DLL do mecanismo de banco de dados for descarregada do processo de host.

A [JET_THREADSTATS](./jet-threadstats-structure.md) estrutura de dados provavelmente será expandida no futuro para conter mais estatísticas. Novas estatísticas serão adicionadas ao final da estrutura e poderão ser recuperadas com um tamanho de buffer de saída maior. A presença de estatísticas adicionais pode ser inferida por um valor cbStruct maior.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008.</p></td>
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
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
