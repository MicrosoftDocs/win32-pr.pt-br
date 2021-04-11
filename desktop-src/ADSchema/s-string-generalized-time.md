---
title: Sintaxe da cadeia de caracteres (tempo generalizado)
description: Um formato de cadeia de caracteres de tempo definido pelos padrões ASN. 1. | Sintaxe da cadeia de caracteres (tempo generalizado)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de cadeia de caracteres (tempo generalizado)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172689"
---
# <a name="stringgeneralized-time-syntax"></a>Sintaxe da cadeia de caracteres (tempo generalizado)

Um formato de cadeia de caracteres de tempo definido pelos padrões ASN. 1. Use essa sintaxe para armazenar valores de tempo no formato Generalized-Time.

O formato para a sintaxe de Generalized-Time é "AAAAMMDDHHMMSS. 0Z". Um exemplo de um valor aceitável é "20010928060000.0 Z". O "Z" indica que não há diferencial de tempo. Active Directory armazena data/hora como GMT (hora de Greenwich). Se nenhum diferencial de tempo for especificado, GMT será o padrão.

Se o tempo for especificado em um fuso horário diferente de GMT, o diferencial entre o fuso horário e o GMT será acrescentado à cadeia de caracteres em vez de "Z" no formato "AAAAMMDDHHMMSS. 0 \[ +/- \] hhmm". Um exemplo de um valor aceitável é "20010928060000.0 + 0200". O diferencial é baseado na fórmula: GMT = local + diferencial.

Para obter mais informações, consulte ISO 8601 e X680.



| Entrada | Valor |
|--------------|----------------------------------------------------------------------------|
| Nome         | Cadeia de caracteres (em tempo geral)                                                   |
| ID da sintaxe    | 2.5.5.11                                                                   |
| ID DO OM        | 24                                                                         |
| Tipo de MAPI    | SYSTIME                                                                    |
| Tipo de ADS     | ADSTYPE \_ \_ hora UTC                                                         |
| Tipo de variante | Data de VT \_                                                                   |
| Tipo SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
