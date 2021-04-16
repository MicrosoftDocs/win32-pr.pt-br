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
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="f3ea0-103">Usando sequências de escape e caracteres de controle</span><span class="sxs-lookup"><span data-stu-id="f3ea0-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="f3ea0-104">Quando um aplicativo converte cadeias de caracteres de ASCII ou de uma [página de código do Windows (ANSI)](code-pages.md) para Unicode, ele deve converter as sequências de escape caractere por caractere em Unicode.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="f3ea0-105">Quando um ASCII ou outro arquivo de texto de 8 bits é convertido em Unicode, há uma chance de que ele seja posteriormente convertido de volta.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="f3ea0-106">Converter sequências de escape em Unicode com base em caractere por caractere, em vez de combiná-las como um único caractere Unicode, torna possível executar a conversão inversa sem a necessidade de reconhecer e analisar as sequências de escape como tal.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="f3ea0-107">Por exemplo, ESC + A deve se tornar 0x001B (ESC), 0x0041 (A), em vez de 0x411B.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="f3ea0-108">Os primeiros valores de código de 32 16 bits em Unicode destinam-se aos caracteres de controle 32.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="f3ea0-109">Essa especificação dá suporte ao uso existente de caracteres de controle para fins de formatação.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="f3ea0-110">Os aplicativos Unicode podem tratar esses caracteres de controle exatamente da mesma forma que tratam seus equivalentes ASCII.</span><span class="sxs-lookup"><span data-stu-id="f3ea0-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3ea0-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3ea0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3ea0-112">Usando caracteres especiais em Unicode</span><span class="sxs-lookup"><span data-stu-id="f3ea0-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



