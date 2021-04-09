---
description: A maioria das operações de cadeia de caracteres pode usar a mesma lógica para Unicode e para páginas de código do Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipos de dados do Windows para cadeias de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011846"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="2da33-103">Tipos de dados do Windows para cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="2da33-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="2da33-104">A maioria das operações de cadeia de caracteres pode usar a mesma lógica para [Unicode](unicode.md) e para [páginas de código do Windows](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="2da33-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="2da33-105">A única diferença é que a unidade básica de operação é um caractere de 16 bits (também conhecido como um caractere largo) para Unicode e um caractere de 8 bits para páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="2da33-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="2da33-106">Os arquivos de cabeçalho do Windows fornecem várias definições de tipo que facilitam a criação de fontes que podem ser compiladas para o Unicode ou para páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="2da33-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="2da33-107">O Windows dá suporte a três conjuntos de tipos de dados de caractere e cadeia de caracteres: um conjunto de definições de tipo genérico que pode compilar para as páginas de código Unicode ou Windows e dois conjuntos de definições de tipo específicas.</span><span class="sxs-lookup"><span data-stu-id="2da33-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="2da33-108">Um conjunto de definições de tipo específico é para uso com Unicode e o outro é para uso com páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="2da33-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="2da33-109">Um aplicativo que usa tipos de dados genéricos pode ser compilado para Unicode simplesmente definindo "UNICODE" antes das instruções **\# include** para os arquivos de cabeçalho ou durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="2da33-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="2da33-110">Novos aplicativos do Windows devem usar Unicode para evitar as inconsistências de páginas de código variadas e simplificar a localização.</span><span class="sxs-lookup"><span data-stu-id="2da33-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="2da33-111">Eles devem ser escritos com tipos de dados genéricos e devem definir "UNICODE" para compilar esses tipos em tipos Unicode.</span><span class="sxs-lookup"><span data-stu-id="2da33-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="2da33-112">Nos poucos lugares em que um aplicativo deve trabalhar com dados de caractere de 8 bits, ele pode fazer uso explícito dos tipos para páginas de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="2da33-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="2da33-113">A capacidade de compilar os tipos genéricos em tipos para páginas de código do Windows existe principalmente para dar suporte a aplicativos herdados.</span><span class="sxs-lookup"><span data-stu-id="2da33-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="2da33-114">Para compilar para páginas de código do Windows, o aplicativo simplesmente omite a definição de UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2da33-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="2da33-115">O exemplo a seguir mostra o método usado nos arquivos de cabeçalho do Windows para definir os três conjuntos de tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="2da33-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="2da33-116">Para a implementação, consulte o arquivo de cabeçalho WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="2da33-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="2da33-117">A letra "T" em uma definição de tipo, por exemplo, TCHAR ou LPTSTR, designa um tipo genérico que pode ser compilado para as páginas de código do Windows ou para o Unicode.</span><span class="sxs-lookup"><span data-stu-id="2da33-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="2da33-118">A letra "W" em uma definição de tipo, por exemplo, WCHAR ou LPWSTR, designa um tipo Unicode.</span><span class="sxs-lookup"><span data-stu-id="2da33-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="2da33-119">Como as páginas de código do Windows são do formulário mais antigo, elas têm definições de tipo simples, como CHAR e LPSTR.</span><span class="sxs-lookup"><span data-stu-id="2da33-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="2da33-120">Para obter uma descrição completa dos tipos de dados no Windows, consulte [tipos de dados do Windows](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="2da33-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da33-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2da33-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da33-122">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="2da33-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
