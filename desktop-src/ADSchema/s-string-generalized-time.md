---
title: Sintaxe string(Generalized-Time)
description: Um formato de cadeia de caracteres de tempo definido pelos padrões ASN.1. | Sintaxe string(Generalized-Time)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema do AD de sintaxe string(Generalized-Time)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580206"
---
# <a name="stringgeneralized-time-syntax"></a>Sintaxe string(Generalized-Time)

Um formato de cadeia de caracteres de tempo definido pelos padrões ASN.1. Use essa sintaxe para armazenar valores de tempo Generalized-Time formato.

O formato da sintaxe Generalized-Time é "AAAAMMDDHHMMSS.0Z". Um exemplo de um valor aceitável é "20010928060000.0Z". O "Z" não indica diferencial de tempo. O Active Directory armazena a data/hora como GMT (Hora Média de Greenwich). Se nenhum diferencial de tempo for especificado, GMT será o padrão.

Se o tempo for especificado em um fuso horário diferente de GMT, o diferencial entre o fuso horário e GMT será anexado à cadeia de caracteres em vez de "Z" no formato "AAAAMMDDHHMMSS.0 \[ +/- \] HHMM". Um exemplo de um valor aceitável é "20010928060000.0+0200". O diferencial é baseado na fórmula: GMT=Local+diferencial.

Para obter mais informações, consulte ISO 8601 e X680.



| Entrada | Valor |
|--------------|----------------------------------------------------------------------------|
| Nome         | String(Generalized-Time)                                                   |
| ID da sintaxe    | 2.5.5.11                                                                   |
| OM ID        | 24                                                                         |
| Tipo MAPI    | SYSTIME                                                                    |
| Tipo ADS     | HORA \_ UTC ADSTYPE \_                                                         |
| Tipo de variante | DATA \_ DA VT                                                                   |
| Tipo de SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
