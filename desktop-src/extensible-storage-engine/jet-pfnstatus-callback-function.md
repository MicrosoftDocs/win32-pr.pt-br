---
description: 'Saiba mais sobre: JET_PFNSTATUS função de retorno de chamada'
title: JET_PFNSTATUS função de retorno de chamada
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170545"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS função de retorno de chamada


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS função de retorno de chamada

A função de retorno de chamada **JET_PFNSTATUS** recebe informações sobre o progresso de operações de longa execução, como operações de desfragmentação, backup ou restauração. Durante essas operações, o mecanismo de banco de dados chama essa função de retorno de chamada para fornecer uma atualização no andamento da operação.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão do tipo [JET_SESID](./jet-sesid.md) com a qual a função de longa execução foi chamada.

*padrões*

O tipo de operação conforme especificado em [JET_SNP](./jet-snp.md). Os tipos de operações incluem reparar, compactar, restaurar, fazer backup, atualizar, depurar e atualizar o formato do registro.

*snt*

O status de uma operação. Os tipos de status incluem início, em andamento, conclusão ou falha. O status será especificado com o terceiro parâmetro do tipo [JET_SNT](./jet-snt.md).

*PV*

Um ponteiro opcional para uma estrutura do tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md). Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

Em caso de sucesso, a operação que emitiu o retorno de chamada pode continuar normalmente. Em alguns casos, o retorno de chamada pode retornar um aviso que influencia essa operação.

Em caso de falha, a operação que emitiu o retorno de chamada pode continuar normalmente ou pode falhar.

### <a name="remarks"></a>Comentários

Essa função de retorno de chamada será usada em uma notificação de progresso, na qual a estrutura indicará o estado atual do progresso. Observe que a função de retorno de chamada pode ser chamada várias vezes para o andamento da operação.

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

[Códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
