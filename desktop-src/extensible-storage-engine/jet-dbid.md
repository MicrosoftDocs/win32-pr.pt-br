---
description: 'Saiba mais sobre: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: 988dd14ca96a5818254602b5ab6dcaeab4952669
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470902"
---
# <a name="jet_dbid"></a>JET_DBID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbid"></a>JET_DBID

O **JET_DBID** de dados contém o identificador para o banco de dados. Um handle de banco de dados é usado para gerenciar o esquema de um banco de dados. Ele também pode ser usado para gerenciar as tabelas dentro desse banco de dados.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipos de dados

JET_DBID

Lidar com o banco de dados.

Um valor de JET_dbidNil indica que o alça é inválido.

### <a name="remarks"></a>Comentários

Um handle de banco de dados é criado por meio de uma chamada para [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md).

Um handle de banco de dados pode ser fechado explicitamente por [JetCloseDatabase](./jetclosedatabase-function.md) ou implicitamente fechado por [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).

Um alça de banco de dados só pode ser usado dentro da sessão em que foi criado. A existência de um alça de banco de dados corresponde à abertura lógica de um banco de dados. Uma abertura lógica é diferente da abertura física de um banco de dados, que acontece quando um banco de dados é anexado ao sistema.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
