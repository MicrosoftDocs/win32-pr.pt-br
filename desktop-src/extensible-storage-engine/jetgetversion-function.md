---
description: 'Saiba mais sobre: função JetGetVersion'
title: Função JetGetVersion
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171621"
---
# <a name="jetgetversion-function"></a>Função JetGetVersion


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetversion-function"></a>Função JetGetVersion

A função **JetGetVersion** recupera a versão do mecanismo de banco de dados.

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*pwVersion*

Um ponteiro para o número de versão do mecanismo de banco de dados.

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
</tbody>
</table>


Se essa função for realizada com sucesso, a versão do mecanismo de banco de dados será recuperada.

Não há modos de falha conhecidos.

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

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)
