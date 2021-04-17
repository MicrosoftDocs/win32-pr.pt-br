---
description: Um identificador de idioma é uma abreviação numérica internacional padrão para o idioma em um país ou região geográfica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificadores de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783287"
---
# <a name="language-identifiers"></a>Identificadores de idioma

Um identificador de idioma é uma abreviação numérica internacional padrão para o [idioma](locales-and-languages.md) em um país ou região geográfica. Cada idioma tem um identificador de idioma exclusivo (tipo de dados LANGid), um valor de 16 bits que consiste em um identificador de idioma primário e um identificador de subidioma. Para obter detalhes sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](language-identifier-constants-and-strings.md).

Um identificador de idioma é construído usando a macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) . A ilustração a seguir mostra o formato dos bits em um identificador de idioma.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Estes são os identificadores de idioma predefinidos:

-   padrão do sistema de idioma \_ \_ . O idioma padrão do sistema operacional.
-   padrão do usuário do idioma \_ \_ . O idioma do usuário atual.

Seu aplicativo pode recuperar os identificadores de idioma atuais usando as funções de [interface do usuário multilíngüe](multilingual-user-interface.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Constantes e cadeias de caracteres de identificador de linguagem](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



