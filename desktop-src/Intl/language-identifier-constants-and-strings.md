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
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="a888f-103">Constantes e cadeias de caracteres de identificador de linguagem</span><span class="sxs-lookup"><span data-stu-id="a888f-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a888f-104">As constantes de identificador de idioma são preteridas e seu uso não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="a888f-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="a888f-105">O uso de nomes de localidade em vez de identificadores de localidade é sempre preferível.</span><span class="sxs-lookup"><span data-stu-id="a888f-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="a888f-106">Consulte [identificador de idioma](language-identifiers.md) para obter uma descrição dos identificadores de idioma.</span><span class="sxs-lookup"><span data-stu-id="a888f-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="a888f-107">Um identificador primário ou de subidioma pode ser definido pelo usuário ou predefinido.</span><span class="sxs-lookup"><span data-stu-id="a888f-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="a888f-108">Para os identificadores de idioma primário predefinidos com seus identificadores de subidioma válidos, consulte [[MS-LCID]: referência de LCID (identificador de código de idioma do Windows)](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="a888f-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="a888f-109">Se não houver nenhum identificador de subidioma para usar com um identificador de idioma primário, seu aplicativo deverá usar o **\_ padrão SUBLANG**.</span><span class="sxs-lookup"><span data-stu-id="a888f-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="a888f-110">Ele deve usar o **SUBLANG \_ neutro** para recursos que são os mesmos para todos os subidiomas de um idioma primário.</span><span class="sxs-lookup"><span data-stu-id="a888f-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="a888f-111">Um identificador de idioma primário definido pelo usuário tem um valor no intervalo de 0x0200 a 0x03FF.</span><span class="sxs-lookup"><span data-stu-id="a888f-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="a888f-112">Todos os outros valores são reservados para uso do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a888f-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="a888f-113">Um identificador de subidioma definido pelo usuário tem um valor no intervalo de 0x20 a 0x3F.</span><span class="sxs-lookup"><span data-stu-id="a888f-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="a888f-114">Todos os outros valores são reservados para uso do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a888f-114">All other values are reserved for operating system use.</span></span>
