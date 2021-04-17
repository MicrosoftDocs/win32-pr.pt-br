---
description: 'Saiba mais sobre: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105812239"
---
# <a name="jet_err"></a>JET_ERR


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

O tipo de dados **JET_ERR** contém um [código de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipos de dados

JET_ERR

Um valor zero (correspondente a JET_errSuccess) indica que a chamada foi bem-sucedida. Um valor positivo avisa sobre uma condição não fatal que ocorreu durante uma chamada com êxito. Um valor negativo indica que a chamada falhou.

### <a name="remarks"></a>Comentários

Para obter informações sobre como retornar erros como HRESULTs, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md). Para obter informações sobre sinalizadores para configurar o banco de dados para lidar com erros, consulte [parâmetros de tratamento de erros](./error-handling-parameters.md).

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

[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[Códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md)  
[Parâmetros de tratamento de erros](./error-handling-parameters.md)
