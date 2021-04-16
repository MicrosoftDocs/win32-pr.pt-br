---
description: 'As funções da API do Windows que manipulam caracteres geralmente são implementadas em um dos três formatos:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode na API do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758135"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="48f8c-103">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="48f8c-103">Unicode in the Windows API</span></span>

<span data-ttu-id="48f8c-104">As funções da API do Windows que manipulam caracteres geralmente são implementadas em um dos três formatos:</span><span class="sxs-lookup"><span data-stu-id="48f8c-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="48f8c-105">Uma versão genérica que pode ser compilada para as páginas de código do Windows ou para o Unicode</span><span class="sxs-lookup"><span data-stu-id="48f8c-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="48f8c-106">Uma versão de [página de código do Windows](code-pages.md) com a letra "a" usada para indicar "ANSI"</span><span class="sxs-lookup"><span data-stu-id="48f8c-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="48f8c-107">Uma versão [Unicode](unicode.md) com a letra "W" usada para indicar "largo"</span><span class="sxs-lookup"><span data-stu-id="48f8c-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="48f8c-108">Algumas funções mais recentes dão suporte apenas a versões Unicode.</span><span class="sxs-lookup"><span data-stu-id="48f8c-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="48f8c-109">Para obter mais informações, consulte [convenções para protótipos de função](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="48f8c-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="48f8c-110">Os tópicos a seguir discutem os tipos de dados Unicode e como eles são usados em funções e mensagens; o uso de recursos, nomes de arquivos e argumentos de linha de comando; e métodos de tradução entre diferentes tipos de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48f8c-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="48f8c-111">Tradução automática de mensagens</span><span class="sxs-lookup"><span data-stu-id="48f8c-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="48f8c-112">Conjuntos de caracteres usados em nomes de arquivo</span><span class="sxs-lookup"><span data-stu-id="48f8c-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="48f8c-113">Argumentos de linha de comando</span><span class="sxs-lookup"><span data-stu-id="48f8c-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="48f8c-114">Convenções para protótipos de função</span><span class="sxs-lookup"><span data-stu-id="48f8c-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="48f8c-115">Funções padrão C</span><span class="sxs-lookup"><span data-stu-id="48f8c-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="48f8c-116">Diferenças de função de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="48f8c-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="48f8c-117">Conversão entre tipos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="48f8c-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="48f8c-118">Tipos de dados do Windows para cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="48f8c-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="48f8c-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48f8c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48f8c-120">Sobre Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="48f8c-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



