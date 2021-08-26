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
ms.openlocfilehash: f341f88a192fee6de55e0077778abde83493e35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482272"
---
# <a name="jet_err"></a>JET_ERR


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_err"></a>JET_ERR

O **JET_ERR** de dados contém um [código de erro extensível Armazenamento Engine](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Tipos de dados

JET_ERR

Um valor zero (correspondente JET_errSuccess) indica que a chamada foi bem-sucedida. Um valor positivo avisa sobre uma condição não fatal que ocorreu durante uma chamada de outra forma bem-sucedida. Um valor negativo indica que a chamada falhou.

### <a name="remarks"></a>Comentários

Para obter informações sobre como retornar erros como HRESULTs, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md). Para obter informações sobre sinalizadores para configurar o banco de dados para tratar erros, consulte [Parâmetros de tratamento de erro](./error-handling-parameters.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[Códigos de erro Armazenamento mecanismo extensível](./extensible-storage-engine-error-codes.md)  
[Parâmetros de tratamento de erro](./error-handling-parameters.md)
