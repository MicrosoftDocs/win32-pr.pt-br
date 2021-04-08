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
# <a name="uniform-resource-locators-urls-in-winhttp"></a>URLs (Uniform Resource Locators) no WinHTTP

Uma URL é uma representação compacta do local e do método de acesso para um recurso localizado na Internet. Cada URL consiste em um esquema (HTTP, HTTPS, FTP ou gopher) e uma cadeia de caracteres específica do esquema. Essa cadeia de caracteres também pode incluir uma combinação de um caminho de diretório, uma cadeia de caracteres de pesquisa ou um nome do recurso. As funções do Microsoft Windows HTTP Services (WinHTTP) fornecem a capacidade de criar, combinar, dividir e gerar URLs em formato canônico. Para obter mais informações, consulte [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [localizadores de recursos uniformes](https://www.ietf.org/rfc/rfc1738.txt) e [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [identificadores de recurso uniforme (URI): sintaxe genérica](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>O que é uma URL canônica?

A sintaxe especificada e a semântica de URLs deixam espaço para variação e erro. A canonização é o processo de normalização de uma URL real em um formulário "canônico" correto, padrão.

Isso envolve codificar alguns caracteres como "sequências de escape". Caracteres alfanuméricos US-ASCII não precisam ser codificados (os dígitos 0-9, as letras maiúsculas A-Z e as letras minúsculas a-z). A maioria dos outros caracteres deve ter escape, incluindo caracteres de controle, o caractere de espaço, o sinal de porcentagem, "caracteres não seguros" (<, >, ", \# , {,},, \| \\ , ^, ~, \[ , \] e") e todos os caracteres com um ponto de código acima de 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Usando as funções WinHTTP para manipular URLs

O WinHTTP fornece duas funções para lidar com URLs. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa uma URL em suas partes de componente e [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) cria uma URL de componentes.

### <a name="separating-urls"></a>Separando URLs

A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separa uma URL em suas partes de componente e retorna os componentes indicados pela estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) que é passada para a função.

Os componentes que compõem a estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) são o número do esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e informações adicionais, como parâmetros de pesquisa. Cada componente, exceto o esquema e os números de porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres. Os números de porta e esquema têm apenas um membro que armazena o valor correspondente; os números de porta e esquema são retornados em todas as chamadas bem-sucedidas para [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).

Para recuperar o valor de um componente específico na estrutura [**de \_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , o membro que armazena o tamanho da cadeia de caracteres desse componente deve ser definido como um valor diferente de zero. O membro da cadeia de caracteres pode ser um ponteiro para um buffer ou **nulo**.

Se o membro do ponteiro contiver um ponteiro para um buffer, o membro de comprimento da cadeia de caracteres deverá conter o tamanho desse buffer. A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) retorna as informações do componente como uma cadeia de caracteres no buffer e armazena o comprimento da cadeia de caracteres no membro de comprimento da cadeia de caracteres.

Se o membro do ponteiro for definido como **NULL**, o membro de comprimento da cadeia de caracteres poderá ser definido como qualquer valor diferente de zero. A função [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) armazena um ponteiro para o primeiro caractere da cadeia de caracteres da URL que contém as informações do componente e define o tamanho da cadeia de caracteres para o número de caracteres na parte restante da cadeia de caracteres da URL que pertence ao componente.

Todos os membros do ponteiro definidos como **NULL** com um ponto de membro de comprimento diferente de zero para o ponto de partida apropriado na cadeia de caracteres da URL. O comprimento armazenado no membro Length deve ser usado para determinar o final das informações do componente individual.

Para concluir a inicialização correta da estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , o membro **dwStructSize** deve ser definido como o tamanho da estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .

### <a name="creating-urls"></a>Criando URLs

A função [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) usa as informações na estrutura de [**\_ componentes de URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) descrita anteriormente para criar uma URL.

Para cada componente necessário, o membro do ponteiro deve conter um ponteiro para o buffer que contém as informações. O membro Length deve ser definido como zero se o membro do ponteiro contiver um ponteiro para uma cadeia de caracteres terminada em zero; o membro Length deve ser definido como o comprimento da cadeia de caracteres se o membro do ponteiro contiver um ponteiro para uma cadeia de caracteres que não seja terminada em zero. O membro de ponteiro de quaisquer componentes que não são necessários deve ser definido como **nulo**.

### <a name="sample-code"></a>Código de exemplo

O código de exemplo a seguir mostra como usar [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) e [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) para desmontar uma URL existente, modificar um de seus componentes e remontá-la em uma nova URL.


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



 

 



