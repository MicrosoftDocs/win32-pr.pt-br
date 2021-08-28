---
description: 'Saiba mais sobre: estrutura de JET_INSTANCE_INFO'
title: Estrutura de JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
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
ms.openlocfilehash: 6dbeab994d012f031de7620487c754b69d00db3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472692"
---
# <a name="jet_instance_info-structure"></a>Estrutura de JET_INSTANCE_INFO


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_instance_info-structure"></a>Estrutura de JET_INSTANCE_INFO

A estrutura de **JET_INSTANCE_INFO** recebe informações sobre a execução de instâncias de banco de dados quando usadas com as funções [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) e [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) .

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Membros

**hInstanceId**

O [JET_INSTANCE](./jet-instance.md) da instância fornecida.

**szInstanceName**

O nome da instância do banco de dados. Esse valor pode ser **nulo** se a instância não tiver um nome.

**cDatabases**

O número de bancos de dados que são anexados à instância de Database. **cDatabases** também mantém o tamanho das matrizes de cadeias de caracteres que são retornadas em **szDatabaseFileName**, **szDatabaseDisplayName** e **szDatabaseSLVFileName**.

**szDatabaseFileName**

Uma matriz de cadeias de caracteres, cada uma mantendo o nome de arquivo de um banco de dados anexado à instância do banco de dados. A matriz tem elementos **cDatabases** .

**szDatabaseDisplayName**

Uma matriz de cadeias de caracteres, cada uma mantendo o nome de exibição de um banco de dados. Atualmente, a cadeia de caracteres pode ser nula. A matriz tem elementos **cDatabases** .

**szDatabaseSLVFileName**

Uma matriz de cadeias de caracteres, cada uma mantendo o nome de arquivo do arquivo SLV que está anexado à instância do banco de dados. A matriz tem elementos **cDatabases** . Não há suporte para arquivos SLV, portanto, esse campo deve ser ignorado.

### <a name="remarks"></a>Comentários

Cada instância de banco de dados pode ter vários bancos de dados anexados a ela.

Para uma determinada estrutura de **JET_INSTANCE_INFO** , a matriz de cadeias de caracteres retornada para os bancos de dados está na mesma ordem. Por exemplo, "szDatabaseDisplayName \[ i \] " e "szDatabaseFileName \[ i \] " fazem referência ao mesmo banco de dados.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_INSTANCE_INFO_W</strong> (Unicode) e <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
