---
description: 'Saiba mais sobre: JET_PFNREALLOC função de retorno de chamada'
title: JET_PFNREALLOC função de retorno de chamada
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172082"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC função de retorno de chamada


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC função de retorno de chamada

A função JET_PFNREALLOC é um retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usado pelo [JetEnumerateColumns](./jetenumeratecolumns-function.md) para alocar memória para seus buffers de saída.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parâmetros

*pvContext*

O ponteiro de contexto fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md). Esse ponteiro de contexto pode ser usado para transmitir o estado do chamador de [JetEnumerateColumns](./jetenumeratecolumns-function.md) para a implementação desse retorno de chamada.

*PV*

Se não for NULL, especifica um ponteiro para um bloco de memória alocado anteriormente por este retorno de chamada. Se for NULL, um novo bloco de memória do tamanho solicitado será alocado.

*CB*

O novo tamanho do bloco de memória em bytes. Se esse parâmetro for 0 (zero) e um bloco de memória for especificado, esse bloco de memória será liberado.

### <a name="return-value"></a>Valor Retornado

O sistema pode gerar códigos de êxito ou de falha como resultado de uma chamada para essa função. Para obter informações sobre como retornar esses códigos como HRESULTs, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md).

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
<td><p>Êxito</p></td>
<td><p>Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho zero for especificado, esse bloco será liberado e nulo será retornado. Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho diferente de zero tiver sido especificado, o bloco de memória realocada será retornado. Se nenhum bloco de memória tiver sido especificado, um bloco de memória recentemente alocado do tamanho especificado será retornado.</p></td>
</tr>
<tr class="even">
<td><p>Falha</p></td>
<td><p>NULL será retornado. Se um bloco de memória alocado anteriormente tiver sido fornecido, esse bloco permanecerá alocado.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

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
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
