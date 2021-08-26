---
description: 'Saiba mais sobre: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: ca4478684e79dfb698dd30bb21132f597129fdac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479332"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_pwstr"></a>JET_PWSTR

O tipo de dados **JET_PWSTR** contém uma cadeia de caracteres **Unicode** terminada em nulo (Char \* ).

**Windows vista: JET_PWSTR** é introduzido no Windows Vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Tipos de dados

JET_PWSTR

Terminação nula, Cadeia de caracteres Unicode (Char \* ).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


