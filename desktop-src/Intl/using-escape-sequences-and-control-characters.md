---
description: Quando um aplicativo converte cadeias de caracteres de ASCII ou de uma página de código do Windows (ANSI) para Unicode, ele deve converter as sequências de escape caractere por caractere em Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Usando sequências de escape e caracteres de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757977"
---
# <a name="using-escape-sequences-and-control-characters"></a>Usando sequências de escape e caracteres de controle

Quando um aplicativo converte cadeias de caracteres de ASCII ou de uma [página de código do Windows (ANSI)](code-pages.md) para Unicode, ele deve converter as sequências de escape caractere por caractere em Unicode. Quando um ASCII ou outro arquivo de texto de 8 bits é convertido em Unicode, há uma chance de que ele seja posteriormente convertido de volta. Converter sequências de escape em Unicode com base em caractere por caractere, em vez de combiná-las como um único caractere Unicode, torna possível executar a conversão inversa sem a necessidade de reconhecer e analisar as sequências de escape como tal. Por exemplo, ESC + A deve se tornar 0x001B (ESC), 0x0041 (A), em vez de 0x411B.

Os primeiros valores de código de 32 16 bits em Unicode destinam-se aos caracteres de controle 32. Essa especificação dá suporte ao uso existente de caracteres de controle para fins de formatação. Os aplicativos Unicode podem tratar esses caracteres de controle exatamente da mesma forma que tratam seus equivalentes ASCII.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



