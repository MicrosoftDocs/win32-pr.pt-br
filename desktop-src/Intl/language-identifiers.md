---
description: Um identificador de idioma é uma abreviação numérica internacional padrão para o idioma em um país ou região geográfica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificadores de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6245101099b5df5c192af60a977ede88412f95cca8afda9270b7aba6e1c41ad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106976"
---
# <a name="language-identifiers"></a>Identificadores de idioma

Um identificador de idioma é uma abreviação numérica internacional padrão para o [idioma](locales-and-languages.md) em um país ou região geográfica. Cada idioma tem um identificador de idioma exclusivo (tipo de dados LANGID), um valor de 16 bits que consiste em um identificador de idioma primário e um identificador de sublânguo. Para obter detalhes dos identificadores de idioma, consulte Constantes e cadeias de caracteres do [identificador de idioma.](language-identifier-constants-and-strings.md)

Um identificador de idioma é construído usando a [**macro MAKELANGID.**](/windows/desktop/api/Winnt/nf-winnt-makelangid) A ilustração a seguir mostra o formato dos bits em um identificador de idioma.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Veja a seguir identificadores de idioma predefinidos:

-   LANG \_ SYSTEM \_ DEFAULT. O idioma padrão do sistema operacional.
-   LANG \_ USER \_ DEFAULT. O idioma do usuário atual.

Seu aplicativo pode recuperar os identificadores de idioma atuais usando as [Interface de Usuário Multilíngue](multilingual-user-interface.md) funções.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Constantes e cadeias de caracteres do identificador de idioma](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



