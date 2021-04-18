---
description: ILANGUAGE de localidade \_
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812927"
---
# <a name="locale_ilanguage"></a>ILANGUAGE de localidade \_

[Identificador de idioma](language-identifiers.md) com um valor hexadecimal. Por exemplo, inglês (Estados Unidos) tem o valor 0409, que indica o hexadecimal 0x0409, e é equivalente a 1033 decimal. O número máximo de caracteres permitido para essa cadeia de caracteres é cinco, incluindo um caractere nulo de terminação.

**Windows Vista e posterior:** O uso dessa constante pode fazer com que [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) retorne um identificador de localidade inválido. Seu aplicativo deve usar a [constante \_ SNAME de localidade](locale-sname.md) ao chamar essa função.

 

 



