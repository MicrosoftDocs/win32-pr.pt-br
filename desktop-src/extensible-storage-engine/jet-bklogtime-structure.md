---
description: 'Saiba mais sobre: estrutura JET_BKLOGTIME dados'
title: estrutura JET_BKLOGTIME de dados
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 2d6f8e3f77d905eb601441ad8ab3ca88bb08f59d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478522"
---
# <a name="jet_bklogtime-structure"></a>estrutura JET_BKLOGTIME de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_bklogtime-structure"></a>estrutura JET_BKLOGTIME de dados

A **JET_BKLOGTIME** estrutura contém os elementos de data e hora de um evento. É uma extensão de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista: JET_BKLOGTIME** é introduzido no Windows Vista.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Membros

**bSeconds**

A hora do evento em segundos. Isso pode ser de 0 (zero) a 60. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**bMinutes**

A hora do evento em minutos. Isso pode ser de 0 (zero) a 60. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**bHours**

A hora do evento em horas. Isso pode ser de 0 (zero) a 24. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**Bday**

O dia do mês do evento. Isso pode ser de 0 (zero) a 31. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**bMonth**

O mês do ano do evento. Isso pode ser de 0 (zero) a 12. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**bYear**

O ano (deslocamento de 1900) do evento. Para atingir o ano real, adicione 1900 a esse valor. 0 (zero) é usado quando a **estrutura JET_BKLOGTIME** é "nula".

**bFiller1**

Esse campo deve ser ignorado.

**fTimeIsUTC**

A hora está no formato UTC.

**fUnused**

Esse campo deve ser ignorado.

**bFiller2**

Esse campo deve ser ignorado.

**fOSSnapshot**

Se esse evento for um backup, esse sinalizador conterá um dos seguintes valores possíveis:


| <p>Nome</p> | <p>Valor</p> | 
|-------------|--------------|
| <p>backup de streaming</p> | <p>0 (zero)</p> | 
| <p>backup de instantâneo</p> | <p>1</p> | 



**fReserved**

Esse campo deve ser ignorado.

### <a name="remarks"></a>Comentários

Essa estrutura é usada durante a depuração.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
