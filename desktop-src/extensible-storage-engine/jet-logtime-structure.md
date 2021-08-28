---
description: 'Saiba mais sobre: estrutura de JET_LOGTIME'
title: Estrutura de JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 4cb99f2a64877ec76afda993a76be4aeaa14c895
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987029"
---
# <a name="jet_logtime-structure"></a>Estrutura de JET_LOGTIME


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_logtime-structure"></a>Estrutura de JET_LOGTIME

A estrutura de **JET_LOGTIME** contém elementos da data e hora de um evento.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Membros

**bSeconds**

A hora do evento em segundos. Esse valor pode ser de 0 a 59. 0 é usado quando a estrutura é nula.

**bMinutes**

A hora do evento em minutos. Esse valor pode ser de 0 a 59. 0 é usado quando a estrutura é nula.

**bHours**

A hora do evento em horas. Esse valor pode ser de 0 a 23. 0 é usado quando a estrutura é nula.

**bDay**

O dia do mês do evento. Esse valor pode ser de 0 a 31. 0 é usado quando a estrutura é nula.

**bMonth**

O mês do ano do evento. Esse valor pode ser de 0 a 12. 0 é usado quando a estrutura é nula.

**bYear**

O ano do evento (offset de 1900). Para obter o ano real, adicione 1900 a esse valor. 0 é usado quando a estrutura é nula.

**bFiller1**

Esse campo deve ser ignorado.

**fTimeIsUTC**

A hora está no formato UTC.

**fUnused**

Esse campo deve ser ignorado.

**bFiller2**

Esse campo deve ser ignorado.

### <a name="remarks"></a>Comentários

Essa estrutura destina-se principalmente ao uso na depuração.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
