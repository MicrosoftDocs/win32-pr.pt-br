---
description: 'Saiba mais sobre: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 6a698afffb415bb4418f46cfe16091ceda03cb59
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985159"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_pcstr"></a>JET_PCSTR

O tipo de dados **JET_PCSTR** contém uma cadeia de caracteres **ASCII** de constante de terminação nula (Char \* ).

**Windows vista: JET_PCSTR** é introduzido no Windows Vista.

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>Tipos de dados

JET_PCSTR

Cadeia de caracteres ASCII de constante terminada em nulo (Char \* ).

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


