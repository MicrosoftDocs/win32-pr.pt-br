---
description: 'Saiba mais sobre: estrutura de JET_SIGNATURE'
title: Estrutura de JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: 456eadecbaba7295753a18ec2ca739f5e3fc8391
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987819"
---
# <a name="jet_signature-structure"></a>Estrutura de JET_SIGNATURE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_signature-structure"></a>Estrutura de JET_SIGNATURE

A estrutura de **JET_SIGNATURE** contém informações que identificam exclusivamente um banco de dados.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Membros

**ulRandom**

Um número atribuído aleatoriamente.

**logtimeCreate**

O [JET_LOGTIME](./jet-logtime-structure.md) no momento da [JetCreateDatabase](./jetcreatedatabase-function.md) é executado.

**szComputerName**

O valor de cadeia de caracteres opcional do nome NetBIOS para o computador. Esse valor não pode ser definido.

### <a name="remarks"></a>Comentários

Isso pode ser encontrado como um elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
