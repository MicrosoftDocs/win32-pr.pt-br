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
ms.openlocfilehash: c576734a3e2da71f041509e5b7d7d9244427dbb8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986689"
---
# <a name="jet_dbid"></a>JET_DBID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_dbid"></a>JET_DBID

O tipo de dados **JET_DBID** contém o identificador para o banco de dado. Um identificador de banco de dados é usado para gerenciar o esquema de um banco de dados. Ele também pode ser usado para gerenciar as tabelas dentro desse banco de dados.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Tipos de dados

JET_DBID

Identificador para o banco de dados.

Um valor de JET_dbidNil indica que o identificador é inválido.

### <a name="remarks"></a>Comentários

Um identificador de banco de dados é criado por meio de uma chamada para [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md).

Um identificador de banco de dados pode ser fechado explicitamente por [JetCloseDatabase](./jetclosedatabase-function.md) ou implicitamente fechado por [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md).

Um identificador de banco de dados pode ser usado somente dentro da sessão em que foi criado. A existência de um identificador de banco de dados corresponde à abertura lógica de um banco de dados. Uma abertura lógica é diferente da abertura física de um banco de dados, o que acontece quando um banco de dados é anexado ao sistema.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
