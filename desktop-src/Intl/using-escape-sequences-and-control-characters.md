---
description: Quando um aplicativo converte cadeias de caracteres de ASCII ou de uma página de código ANSI (Windows) para Unicode, ele deve converter sequências de escape caractere por caractere em Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Usando sequências de escape e caracteres de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea89997a8f94a9fdd573b2c8360dbdd5342d38ca8bd2e7a133aa29943c07e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389915"
---
# <a name="using-escape-sequences-and-control-characters"></a>Usando sequências de escape e caracteres de controle

Quando um aplicativo converte cadeias de caracteres de ASCII ou de uma página de código [ANSI (Windows)](code-pages.md) para Unicode, ele deve converter sequências de escape caractere por caractere em Unicode. Quando um ASCII ou outro arquivo de texto de 8 bits é convertido em Unicode, há uma chance de que ele seja convertido posteriormente de volta. Converter sequências de escape em Unicode em uma base de caractere por caractere, em vez de combiná-las como um único caractere Unicode, possibilita executar a conversão inversa sem a necessidade de reconhecer e analisar as sequências de escape como tal. Por exemplo, ESC+A deve se tornar 0x001B (ESC), 0x0041 (A), em vez de 0x411B.

Os primeiros valores de código de 32 16 bits em Unicode destinam-se aos 32 caracteres de controle. Essa especificação dá suporte ao uso existente de caracteres de controle para fins de formatação. Os aplicativos Unicode podem tratar esses caracteres de controle exatamente da mesma maneira que tratam seus equivalentes ASCII.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



