---
description: Cada identificador de idioma é composto por um identificador de idioma primário que indica o idioma e um identificador de subidioma que indica o país/região.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes e cadeias de caracteres de identificador de linguagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296857"
---
# <a name="language-identifier-constants-and-strings"></a>Constantes e cadeias de caracteres de identificador de linguagem

> [!IMPORTANT]
> As constantes de identificador de idioma são preteridas e seu uso não é recomendado. O uso de nomes de localidade em vez de identificadores de localidade é sempre preferível.

Consulte [identificador de idioma](language-identifiers.md) para obter uma descrição dos identificadores de idioma.

Um identificador primário ou de subidioma pode ser definido pelo usuário ou predefinido. Para os identificadores de idioma primário predefinidos com seus identificadores de subidioma válidos, consulte [[MS-LCID]: referência de LCID (identificador de código de idioma do Windows)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).

> [!Note]  
> Se não houver nenhum identificador de subidioma para usar com um identificador de idioma primário, seu aplicativo deverá usar o **\_ padrão SUBLANG**. Ele deve usar o **SUBLANG \_ neutro** para recursos que são os mesmos para todos os subidiomas de um idioma primário.

Um identificador de idioma primário definido pelo usuário tem um valor no intervalo de 0x0200 a 0x03FF. Todos os outros valores são reservados para uso do sistema operacional.

Um identificador de subidioma definido pelo usuário tem um valor no intervalo de 0x20 a 0x3F. Todos os outros valores são reservados para uso do sistema operacional.
