---
description: Uma URL é uma representação compacta do local e do método de acesso para um recurso localizado na Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: URLs (Uniform Resource Locators) no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010824"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="adca7-103">URLs (Uniform Resource Locators) no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="adca7-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="adca7-104">Uma URL é uma representação compacta do local e do método de acesso para um recurso localizado na Internet.</span><span class="sxs-lookup"><span data-stu-id="adca7-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="adca7-105">Cada URL consiste em um esquema (HTTP, HTTPS, FTP ou gopher) e uma cadeia de caracteres específica do esquema.</span><span class="sxs-lookup"><span data-stu-id="adca7-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="adca7-106">Essa cadeia de caracteres também pode incluir uma combinação de um caminho de diretório, uma cadeia de caracteres de pesquisa ou um nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="adca7-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="adca7-107">As funções do Microsoft Windows HTTP Services (WinHTTP) fornecem a capacidade de criar, combinar, dividir e gerar URLs em formato canônico.</span><span class="sxs-lookup"><span data-stu-id="adca7-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="adca7-108">Para obter mais informações, consulte [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [localizadores de recursos uniformes](https://www.ietf.org/rfc/rfc1738.txt) e [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [identificadores de recurso uniforme (URI): sintaxe genérica](https://www.ietf.org/rfc/rfc1738.txt).</span><span class="sxs-lookup"><span data-stu-id="adca7-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="adca7-109">O que é uma URL canônica?</span><span class="sxs-lookup"><span data-stu-id="adca7-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="adca7-110">A sintaxe especificada e a semântica de URLs deixam espaço para variação e erro.</span><span class="sxs-lookup"><span data-stu-id="adca7-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="adca7-111">A canonização é o processo de normalização de uma URL real em um formulário "canônico" correto, padrão.</span><span class="sxs-lookup"><span data-stu-id="adca7-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="adca7-112">Isso envolve codificar alguns caracteres como "sequências de escape".</span><span class="sxs-lookup"><span data-stu-id="adca7-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="adca7-113">Caracteres alfanuméricos US-ASCII não precisam ser codificados (os dígitos 0-9, as letras maiúsculas A-Z e as letras minúsculas a-z).</span><span class="sxs-lookup"><span data-stu-id="adca7-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="adca7-114">A maioria dos outros caracteres deve ter escape, incluindo caracteres de controle, o caractere de espaço, o sinal de porcentagem, "caracteres não seguros" (<, >, ", \# , {,},, \| \\ , ^, ~, \[ , \] e") e todos os caracteres com um ponto de código acima de 127.</span><span class="sxs-lookup"><span data-stu-id="adca7-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="adca7-115">Usando as funções WinHTTP para manipular URLs</span><span class="sxs-lookup"><span data-stu-id="adca7-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="adca7-116">O WinHTTP fornece duas funções para lidar com URLs.</span><span class="sxs-lookup"><span data-stu-id="adca7-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="adca7-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa uma URL em suas partes de componente e [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) cria uma URL de componentes.</span><span class="sxs-lookup"><span data-stu-id="adca7-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="adca7-118">Separando URLs</span><span class="sxs-lookup"><span data-stu-id="adca7-118">Separating URLs</span></span>

<span data-ttu-id="adca7-119">A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa uma URL em suas partes de componente e retorna os componentes indicados pela estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) que é passada para a função.</span><span class="sxs-lookup"><span data-stu-id="adca7-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="adca7-120">Os componentes que compõem a estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) são o número do esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e informações adicionais, como parâmetros de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="adca7-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="adca7-121">Cada componente, exceto o esquema e os números de porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="adca7-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="adca7-122">Os números de porta e esquema têm apenas um membro que armazena o valor correspondente; os números de porta e esquema são retornados em todas as chamadas bem-sucedidas para [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span><span class="sxs-lookup"><span data-stu-id="adca7-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="adca7-123">Para recuperar o valor de um componente específico na estrutura [**de \_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , o membro que armazena o tamanho da cadeia de caracteres desse componente deve ser definido como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="adca7-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="adca7-124">O membro da cadeia de caracteres pode ser um ponteiro para um buffer ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="adca7-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="adca7-125">Se o membro do ponteiro contiver um ponteiro para um buffer, o membro de comprimento da cadeia de caracteres deverá conter o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="adca7-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="adca7-126">A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) retorna as informações do componente como uma cadeia de caracteres no buffer e armazena o comprimento da cadeia de caracteres no membro de comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="adca7-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="adca7-127">Se o membro do ponteiro for definido como **NULL**, o membro de comprimento da cadeia de caracteres poderá ser definido como qualquer valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="adca7-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="adca7-128">A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) armazena um ponteiro para o primeiro caractere da cadeia de caracteres da URL que contém as informações do componente e define o tamanho da cadeia de caracteres para o número de caracteres na parte restante da cadeia de caracteres da URL que pertence ao componente.</span><span class="sxs-lookup"><span data-stu-id="adca7-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="adca7-129">Todos os membros do ponteiro definidos como **NULL** com um ponto de membro de comprimento diferente de zero para o ponto de partida apropriado na cadeia de caracteres da URL.</span><span class="sxs-lookup"><span data-stu-id="adca7-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="adca7-130">O comprimento armazenado no membro Length deve ser usado para determinar o final das informações do componente individual.</span><span class="sxs-lookup"><span data-stu-id="adca7-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="adca7-131">Para concluir a inicialização correta da estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , o membro **dwStructSize** deve ser definido como o tamanho da estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .</span><span class="sxs-lookup"><span data-stu-id="adca7-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="adca7-132">Criando URLs</span><span class="sxs-lookup"><span data-stu-id="adca7-132">Creating URLs</span></span>

<span data-ttu-id="adca7-133">A função [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa as informações na estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descrita anteriormente para criar uma URL.</span><span class="sxs-lookup"><span data-stu-id="adca7-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="adca7-134">Para cada componente necessário, o membro do ponteiro deve conter um ponteiro para o buffer que contém as informações.</span><span class="sxs-lookup"><span data-stu-id="adca7-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="adca7-135">O membro Length deve ser definido como zero se o membro do ponteiro contiver um ponteiro para uma cadeia de caracteres terminada em zero; o membro Length deve ser definido como o comprimento da cadeia de caracteres se o membro do ponteiro contiver um ponteiro para uma cadeia de caracteres que não seja terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="adca7-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="adca7-136">O membro de ponteiro de quaisquer componentes que não são necessários deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="adca7-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="adca7-137">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="adca7-137">Sample code</span></span>

<span data-ttu-id="adca7-138">O código de exemplo a seguir mostra como usar [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) para desmontar uma URL existente, modificar um de seus componentes e remontá-la em uma nova URL.</span><span class="sxs-lookup"><span data-stu-id="adca7-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



