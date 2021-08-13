---
description: 'Saiba mais sobre: Função JetGetInstanceMiscInfo'
title: Função JetGetInstanceMiscInfo
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ada8dfcd69a4e1933bcb60756d1b812f3b358cd37a3cda914819d2a9f6f4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472346"
---
# <a name="jetgetinstancemiscinfo-function"></a>Função JetGetInstanceMiscInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetinstancemiscinfo-function"></a>Função JetGetInstanceMiscInfo

A **função JetGetInstanceMiscInfo** recupera informações sobre a instância, enquanto a instância está online.

**Windows Vista: JetGetInstanceMiscInfo** é introduzido no Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

Identifica a instância de banco de dados que será usada para a chamada à API.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer depende de *InfoLevel.* O chamador é responsável por alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult.*

*InfoLevel*

Determina que tipo de informações serão recuperadas para a instância especificada pela *instância*. O formato dos dados armazenados em *pvResult* depende *de InfoLevel.*

As opções a seguir estão disponíveis para uso com esse parâmetro.

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult</em> é interpretado como uma <a href="gg269340(v=exchg.10).md">estrutura JET_SIGNATURE</a> da sequência de log de transações associada a essa instância.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>O buffer era muito pequeno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Foi especificado um <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> ou <em>um InfoLevel</em> inválido.</p></td>
</tr>
</tbody>
</table>


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
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
