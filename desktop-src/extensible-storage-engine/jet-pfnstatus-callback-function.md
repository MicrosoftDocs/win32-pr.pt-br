---
description: 'Saiba mais sobre: função JET_PFNSTATUS retorno de chamada'
title: JET_PFNSTATUS de retorno de chamada
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
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482912"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS de retorno de chamada


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS de retorno de chamada

A **JET_PFNSTATUS** de retorno de chamada recebe informações sobre o progresso de operações de longa execução, como operações de desfragmentação, backup ou restauração. Durante essas operações, o mecanismo de banco de dados chama essa função de retorno de chamada para atualizar o progresso da operação.

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

A sessão do tipo [JET_SESID](./jet-sesid.md) com a qual a função de execução longa foi chamada.

*Snp*

O tipo de operação conforme especificado [em JET_SNP](./jet-snp.md). Os tipos de operações incluem reparar, compactar, restaurar, fazer backup, atualizar, limpar e atualizar o formato do registro.

*Snt*

O status de uma operação. Os tipos de status incluem início, em andamento, conclusão ou falha. O status será especificado com o terceiro parâmetro do tipo [JET_SNT](./jet-snt.md).

*Pv*

Um ponteiro opcional para uma estrutura do tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos [códigos de erro do Mecanismo Armazenamento Extensível](./extensible-storage-engine-error-codes.md). Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

Em caso de êxito, a operação que emitiu o retorno de chamada pode continuar normalmente. Em alguns casos, o retorno de chamada pode retornar um aviso que influencia essa operação.

Em caso de falha, a operação que emitiu o retorno de chamada pode continuar normalmente ou pode falhar.

### <a name="remarks"></a>Comentários

Essa função de retorno de chamada será usada em uma notificação de progresso na qual a estrutura indicará o estado atual do progresso. Observe que a função de retorno de chamada pode ser chamada várias vezes para o progresso da operação.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[Códigos de erro Armazenamento mecanismo extensível](./extensible-storage-engine-error-codes.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
