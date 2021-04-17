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
# <a name="language-identifiers"></a><span data-ttu-id="7a205-103">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="7a205-103">Language Identifiers</span></span>

<span data-ttu-id="7a205-104">Um identificador de idioma é uma abreviação numérica internacional padrão para o [idioma](locales-and-languages.md) em um país ou região geográfica.</span><span class="sxs-lookup"><span data-stu-id="7a205-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="7a205-105">Cada idioma tem um identificador de idioma exclusivo (tipo de dados LANGid), um valor de 16 bits que consiste em um identificador de idioma primário e um identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="7a205-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="7a205-106">Para obter detalhes sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](language-identifier-constants-and-strings.md).</span><span class="sxs-lookup"><span data-stu-id="7a205-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="7a205-107">Um identificador de idioma é construído usando a macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) .</span><span class="sxs-lookup"><span data-stu-id="7a205-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="7a205-108">A ilustração a seguir mostra o formato dos bits em um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="7a205-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="7a205-109">Estes são os identificadores de idioma predefinidos:</span><span class="sxs-lookup"><span data-stu-id="7a205-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="7a205-110">padrão do sistema de idioma \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7a205-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="7a205-111">O idioma padrão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7a205-111">The operating system default language.</span></span>
-   <span data-ttu-id="7a205-112">padrão do usuário do idioma \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7a205-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="7a205-113">O idioma do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="7a205-113">The language of the current user.</span></span>

<span data-ttu-id="7a205-114">Seu aplicativo pode recuperar os identificadores de idioma atuais usando as funções de [interface do usuário multilíngüe](multilingual-user-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7a205-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a205-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a205-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a205-116">Localidades e idiomas</span><span class="sxs-lookup"><span data-stu-id="7a205-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="7a205-117">Constantes e cadeias de caracteres de identificador de linguagem</span><span class="sxs-lookup"><span data-stu-id="7a205-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="7a205-118">Interface do Usuário Multilíngue</span><span class="sxs-lookup"><span data-stu-id="7a205-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="7a205-119">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="7a205-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



