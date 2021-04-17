---
title: Manipulando localizadores de recursos uniformes
description: Um Uniform Resource Locator (URL) é uma representação compacta do local e do método de acesso para um recurso localizado na Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104565361"
---
# <a name="handling-uniform-resource-locators"></a><span data-ttu-id="67491-103">Manipulando localizadores de recursos uniformes</span><span class="sxs-lookup"><span data-stu-id="67491-103">Handling Uniform Resource Locators</span></span>

<span data-ttu-id="67491-104">Um Uniform Resource Locator (URL) é uma representação compacta do local e do método de acesso para um recurso localizado na Internet.</span><span class="sxs-lookup"><span data-stu-id="67491-104">A Uniform Resource Locator (URL) is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="67491-105">Cada URL consiste em um esquema (HTTP, HTTPS ou FTP) e uma cadeia de caracteres específica do esquema.</span><span class="sxs-lookup"><span data-stu-id="67491-105">Each URL consists of a scheme (HTTP, HTTPS, or FTP) and a scheme-specific string.</span></span> <span data-ttu-id="67491-106">Essa cadeia de caracteres também pode incluir uma combinação de um caminho de diretório, uma cadeia de caracteres de pesquisa ou um nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="67491-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="67491-107">As funções do WinINet fornecem a capacidade de criar, combinar, dividir e gerar URLs em formato canônico.</span><span class="sxs-lookup"><span data-stu-id="67491-107">The WinINet functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="67491-108">Para obter mais informações sobre URLs, consulte [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) em Uniform Resource Locators (URL).</span><span class="sxs-lookup"><span data-stu-id="67491-108">For more information on URLs, see [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) on Uniform Resource Locators (URL).</span></span>

<span data-ttu-id="67491-109">As funções de URL operam de maneira orientada a tarefas.</span><span class="sxs-lookup"><span data-stu-id="67491-109">The URL functions operate in a task-oriented manner.</span></span> <span data-ttu-id="67491-110">O conteúdo e o formato da URL que é atribuída à função não são verificados.</span><span class="sxs-lookup"><span data-stu-id="67491-110">The content and format of the URL that is given to the function is not verified.</span></span> <span data-ttu-id="67491-111">O aplicativo de chamada deve controlar o uso dessas funções para garantir que os dados estejam no formato pretendido.</span><span class="sxs-lookup"><span data-stu-id="67491-111">The calling application should track the use of these functions to ensure that the data is in the intended format.</span></span> <span data-ttu-id="67491-112">Por exemplo, a função [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) converteria o caractere "%" na sequência de escape "%25" ao usar nenhum sinalizador.</span><span class="sxs-lookup"><span data-stu-id="67491-112">For example, the [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function would convert the character "%" into the escape sequence "%25" when using no flags.</span></span> <span data-ttu-id="67491-113">Se [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) for usado na URL canônica, a sequência de escape "%25" seria convertida na sequência de escape "%2525", que não funcionaria corretamente.</span><span class="sxs-lookup"><span data-stu-id="67491-113">If [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) is used on the canonicalized URL, the escape sequence "%25" would be converted into the escape sequence "%2525", which would not work properly.</span></span>

-   [<span data-ttu-id="67491-114">O que é uma URL canônica?</span><span class="sxs-lookup"><span data-stu-id="67491-114">What Is a Canonicalized URL?</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="67491-115">Usando as funções WinINet para tratar URLs</span><span class="sxs-lookup"><span data-stu-id="67491-115">Using the WinINet Functions to Handle URLs</span></span>](#using-the-wininet-functions-to-handle-urls)
-   [<span data-ttu-id="67491-116">Padronizar URLs</span><span class="sxs-lookup"><span data-stu-id="67491-116">Canonicalizing URLs</span></span>](#what-is-a-canonicalized-url)
-   [<span data-ttu-id="67491-117">Combinando URLs de base e relativas</span><span class="sxs-lookup"><span data-stu-id="67491-117">Combining Base and Relative URLs</span></span>](#combining-base-and-relative-urls)
-   [<span data-ttu-id="67491-118">URLs de violação</span><span class="sxs-lookup"><span data-stu-id="67491-118">Cracking URLs</span></span>](#cracking-urls)
-   [<span data-ttu-id="67491-119">Criando URLs</span><span class="sxs-lookup"><span data-stu-id="67491-119">Creating URLs</span></span>](#creating-urls)
-   [<span data-ttu-id="67491-120">Acessando URLs diretamente</span><span class="sxs-lookup"><span data-stu-id="67491-120">Accessing URLs Directly</span></span>](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="67491-121">O que é uma URL canônica?</span><span class="sxs-lookup"><span data-stu-id="67491-121">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="67491-122">O formato de todas as URLs deve seguir a sintaxe aceita e a semântica para acessar recursos através da Internet.</span><span class="sxs-lookup"><span data-stu-id="67491-122">The format of all URLs must follow the accepted syntax and semantics in order to access resources through the Internet.</span></span> <span data-ttu-id="67491-123">A canonização é o processo de formatação de uma URL para seguir essa sintaxe e semântica aceitas.</span><span class="sxs-lookup"><span data-stu-id="67491-123">Canonicalization is the process of formatting a URL to follow this accepted syntax and semantics.</span></span>

<span data-ttu-id="67491-124">Os caracteres que devem ser codificados incluem todos os caracteres que não têm nenhum caractere gráfico correspondente no conjunto de caracteres codificado US-ASCII (hexadecimal 80-FF, que não são usados no conjunto de caracteres codificados US-ASCII, e hexadecimal 00-1F e 7F, que são caracteres de controle), espaços em branco, "%" (que é usado para codificar outros caracteres) e caracteres não seguros (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] e ').</span><span class="sxs-lookup"><span data-stu-id="67491-124">Characters that must be encoded include any characters that have no corresponding graphic character in the US-ASCII coded character set (hexadecimal 80-FF, which are not used in the US-ASCII coded character set, and hexadecimal 00-1F and 7F, which are control characters), blank spaces, "%" (which is used to encode other characters), and unsafe characters (<, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ').</span></span>

## <a name="using-the-wininet-functions-to-handle-urls"></a><span data-ttu-id="67491-125">Usando as funções WinINet para tratar URLs</span><span class="sxs-lookup"><span data-stu-id="67491-125">Using the WinINet Functions to Handle URLs</span></span>

<span data-ttu-id="67491-126">A tabela a seguir resume as funções de URL.</span><span class="sxs-lookup"><span data-stu-id="67491-126">The following table summarizes the URL functions.</span></span>



| <span data-ttu-id="67491-127">Função</span><span class="sxs-lookup"><span data-stu-id="67491-127">Function</span></span>                                                   | <span data-ttu-id="67491-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="67491-128">Description</span></span>                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="67491-129">**InternetCanonicalizeUrl**</span><span class="sxs-lookup"><span data-stu-id="67491-129">**InternetCanonicalizeUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | <span data-ttu-id="67491-130">Canonicalizes a URL.</span><span class="sxs-lookup"><span data-stu-id="67491-130">Canonicalizes the URL.</span></span>                             |
| [<span data-ttu-id="67491-131">**InternetCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="67491-131">**InternetCombineUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | <span data-ttu-id="67491-132">Combina URLs base e relativas.</span><span class="sxs-lookup"><span data-stu-id="67491-132">Combines base and relative URLs.</span></span>                   |
| [<span data-ttu-id="67491-133">**InternetCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="67491-133">**InternetCrackUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | <span data-ttu-id="67491-134">Analisa uma cadeia de caracteres de URL em componentes.</span><span class="sxs-lookup"><span data-stu-id="67491-134">Parses a URL string into components.</span></span>               |
| [<span data-ttu-id="67491-135">**InternetCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="67491-135">**InternetCreateUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | <span data-ttu-id="67491-136">Cria uma cadeia de caracteres de URL a partir de componentes.</span><span class="sxs-lookup"><span data-stu-id="67491-136">Creates a URL string from components.</span></span>              |
| [<span data-ttu-id="67491-137">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="67491-137">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | <span data-ttu-id="67491-138">Inicia a recuperação de um recurso FTP, HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="67491-138">Begins retrieving an FTP, HTTP, or HTTPS resource.</span></span> |



 

## <a name="canonicalizing-urls"></a><span data-ttu-id="67491-139">Padronizar URLs</span><span class="sxs-lookup"><span data-stu-id="67491-139">Canonicalizing URLs</span></span>

<span data-ttu-id="67491-140">A canonização de uma URL é o processo que converte uma URL, que pode conter caracteres não seguros, como espaços em branco, caracteres reservados e assim por diante, em um formato aceito.</span><span class="sxs-lookup"><span data-stu-id="67491-140">Canonicalizing a URL is the process that converts a URL, which might contain unsafe characters such as blank spaces, reserved characters, and so on, into an accepted format.</span></span>

<span data-ttu-id="67491-141">A função [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) pode ser usada para padronizar URLs.</span><span class="sxs-lookup"><span data-stu-id="67491-141">The [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) function can be used to canonicalize URLs.</span></span> <span data-ttu-id="67491-142">Essa função é muito orientada a tarefas, portanto o aplicativo deve controlar seu uso com cuidado.</span><span class="sxs-lookup"><span data-stu-id="67491-142">This function is very task-oriented, so the application should track its use carefully.</span></span> <span data-ttu-id="67491-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) não verifica se a URL passada para ela já é canônica e se a URL que ela retorna é válida.</span><span class="sxs-lookup"><span data-stu-id="67491-143">[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) does not verify that the URL passed to it is already canonicalized and that the URL that it returns is valid.</span></span>

<span data-ttu-id="67491-144">Os cinco sinalizadores a seguir controlam como o [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) MANIPULA uma URL específica.</span><span class="sxs-lookup"><span data-stu-id="67491-144">The following five flags control how [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) handles a particular URL.</span></span> <span data-ttu-id="67491-145">Os sinalizadores podem ser usados em combinação.</span><span class="sxs-lookup"><span data-stu-id="67491-145">The flags can be used in combination.</span></span> <span data-ttu-id="67491-146">Se nenhum sinalizador for usado, a função codificará a URL por padrão.</span><span class="sxs-lookup"><span data-stu-id="67491-146">If no flags are used, the function encodes the URL by default.</span></span>



| <span data-ttu-id="67491-147">Valor</span><span class="sxs-lookup"><span data-stu-id="67491-147">Value</span></span>                     | <span data-ttu-id="67491-148">Significado</span><span class="sxs-lookup"><span data-stu-id="67491-148">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67491-149">\_modo de navegador ICU \_</span><span class="sxs-lookup"><span data-stu-id="67491-149">ICU\_BROWSER\_MODE</span></span>        | <span data-ttu-id="67491-150">Não codifique nem decodifique caracteres após " \# " ou "?" e não remova o espaço em branco à direita após "?".</span><span class="sxs-lookup"><span data-stu-id="67491-150">Do not encode or decode characters after "\#" or "?", and do not remove trailing white space after "?".</span></span> <span data-ttu-id="67491-151">Se esse valor não for especificado, a URL inteira será codificada e o espaço em branco à direita será removido.</span><span class="sxs-lookup"><span data-stu-id="67491-151">If this value is not specified, the entire URL is encoded, and trailing white space is removed.</span></span> |
| <span data-ttu-id="67491-152">decodificação ICU \_</span><span class="sxs-lookup"><span data-stu-id="67491-152">ICU\_DECODE</span></span>               | <span data-ttu-id="67491-153">Converta todas as% XX sequências em caracteres, incluindo sequências de escape, antes de a URL ser analisada.</span><span class="sxs-lookup"><span data-stu-id="67491-153">Convert all %XX sequences to characters, including escape sequences, before the URL is parsed.</span></span>                                                                                                          |
| <span data-ttu-id="67491-154">\_ \_ somente espaços de codificação ICU \_</span><span class="sxs-lookup"><span data-stu-id="67491-154">ICU\_ENCODE\_SPACES\_ONLY</span></span> | <span data-ttu-id="67491-155">Codificar somente espaços.</span><span class="sxs-lookup"><span data-stu-id="67491-155">Encode spaces only.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="67491-156">ICU \_ sem \_ codificação</span><span class="sxs-lookup"><span data-stu-id="67491-156">ICU\_NO\_ENCODE</span></span>           | <span data-ttu-id="67491-157">Não converta caracteres não seguros em sequências de escape.</span><span class="sxs-lookup"><span data-stu-id="67491-157">Do not convert unsafe characters to escape sequences.</span></span>                                                                                                                                                   |
| <span data-ttu-id="67491-158">ICU \_ sem \_ meta</span><span class="sxs-lookup"><span data-stu-id="67491-158">ICU\_NO\_META</span></span>             | <span data-ttu-id="67491-159">Não remova as metasequências (como "." e "..") da URL.</span><span class="sxs-lookup"><span data-stu-id="67491-159">Do not remove meta sequences (such as "." and "..") from the URL.</span></span>                                                                                                                                       |



 

<span data-ttu-id="67491-160">O \_ sinalizador de decodificação ICU deve ser usado somente em URLs canônicas, pois supõe que todas as sequências de% XX são códigos de escape e as converte nos caracteres indicados pelo código.</span><span class="sxs-lookup"><span data-stu-id="67491-160">The ICU\_DECODE flag should be used only on canonicalized URLs, because it assumes that all %XX sequences are escape codes and converts them into the characters indicated by the code.</span></span> <span data-ttu-id="67491-161">Se a URL tiver um símbolo "%" que não faz parte de um código de escape, a \_ decodificação ICU ainda a tratará como uma.</span><span class="sxs-lookup"><span data-stu-id="67491-161">If the URL has a "%" symbol in it that is not part of an escape code, ICU\_DECODE still treats it as one.</span></span> <span data-ttu-id="67491-162">Essa característica pode fazer com que o [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) crie uma URL inválida.</span><span class="sxs-lookup"><span data-stu-id="67491-162">This characteristic might cause [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to create an invalid URL.</span></span>

<span data-ttu-id="67491-163">Para usar [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) para retornar uma URL completamente decodificada, os \_ sinalizadores de codificação ICU e ICU \_ sem \_ codificação devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="67491-163">To use [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) to return a completely decoded URL, the ICU\_DECODE and ICU\_NO\_ENCODE flags must be specified.</span></span> <span data-ttu-id="67491-164">Essa configuração pressupõe que a URL que está sendo passada para [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) tenha sido anteriormente canônica.</span><span class="sxs-lookup"><span data-stu-id="67491-164">This setup assumes that the URL being passed to [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) has been previously canonicalized.</span></span>

## <a name="combining-base-and-relative-urls"></a><span data-ttu-id="67491-165">Combinando URLs de base e relativas</span><span class="sxs-lookup"><span data-stu-id="67491-165">Combining Base and Relative URLs</span></span>

<span data-ttu-id="67491-166">Uma URL relativa é uma representação compacta do local de um recurso em relação a uma URL base absoluta.</span><span class="sxs-lookup"><span data-stu-id="67491-166">A relative URL is a compact representation of the location of a resource relative to an absolute base URL.</span></span> <span data-ttu-id="67491-167">A URL base deve ser conhecida pelo analisador e geralmente inclui o esquema, o local de rede e as partes do caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="67491-167">The base URL must be known to the parser and usually includes the scheme, network location, and parts of the URL path.</span></span> <span data-ttu-id="67491-168">Um aplicativo pode chamar [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) para combinar a URL relativa com sua URL base.</span><span class="sxs-lookup"><span data-stu-id="67491-168">An application can call [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) to combine the relative URL with its base URL.</span></span> <span data-ttu-id="67491-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) também CANONICALIZES a URL resultante.</span><span class="sxs-lookup"><span data-stu-id="67491-169">[**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) also canonicalizes the resultant URL.</span></span>

## <a name="cracking-urls"></a><span data-ttu-id="67491-170">URLs de violação</span><span class="sxs-lookup"><span data-stu-id="67491-170">Cracking URLs</span></span>

<span data-ttu-id="67491-171">A função [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa uma URL em suas partes de componente e retorna os componentes indicados pela estrutura de [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) que é passada para a função.</span><span class="sxs-lookup"><span data-stu-id="67491-171">The [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure that is passed to the function.</span></span>

<span data-ttu-id="67491-172">Os componentes que compõem a estrutura de [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) são o número do esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e informações adicionais (como parâmetros de pesquisa).</span><span class="sxs-lookup"><span data-stu-id="67491-172">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme number, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="67491-173">Cada componente, exceto o esquema e os números de porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="67491-173">Each component, except the scheme and port numbers, has a string member that holds the information, and a member that holds the length of the string member.</span></span> <span data-ttu-id="67491-174">Os números de porta e esquema têm apenas um membro que armazena o valor correspondente; Elas são retornadas em todas as chamadas bem-sucedidas para [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span><span class="sxs-lookup"><span data-stu-id="67491-174">The scheme and port numbers have only a member that stores the corresponding value; they are both returned on all successful calls to [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).</span></span>

<span data-ttu-id="67491-175">Para obter o valor de um componente específico na estrutura [**de \_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , o membro que armazena o tamanho da cadeia de caracteres desse componente deve ser definido como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="67491-175">To get the value of a particular component in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="67491-176">O membro da cadeia de caracteres pode ser o endereço de um buffer ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="67491-176">The string member can be either the address of a buffer or **NULL**.</span></span>

<span data-ttu-id="67491-177">Se o membro do ponteiro contiver o endereço de um buffer, o membro de comprimento da cadeia de caracteres deverá conter o tamanho desse buffer.</span><span class="sxs-lookup"><span data-stu-id="67491-177">If the pointer member contains the address of a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="67491-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) retorna as informações do componente como uma cadeia de caracteres no buffer e armazena o comprimento da cadeia de caracteres no membro de comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="67491-178">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="67491-179">Se o membro do ponteiro for **nulo**, o membro do comprimento da cadeia de caracteres poderá ser definido como qualquer valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="67491-179">If the pointer member is **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="67491-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) armazena o endereço do primeiro caractere da cadeia de caracteres da URL que contém as informações do componente e define o tamanho da cadeia de caracteres para o número de personagens na parte restante da cadeia de caracteres da URL que pertence ao componente.</span><span class="sxs-lookup"><span data-stu-id="67491-180">[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stores the address of the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="67491-181">Todos os membros do ponteiro definidos como **NULL** com um ponto de membro de comprimento diferente de zero para o ponto de partida apropriado na cadeia de caracteres da URL.</span><span class="sxs-lookup"><span data-stu-id="67491-181">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="67491-182">O comprimento armazenado no membro Length deve ser usado para determinar o final das informações do componente individual.</span><span class="sxs-lookup"><span data-stu-id="67491-182">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="67491-183">Para concluir a inicialização correta da estrutura de [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , o membro **dwStructSize** deve ser definido como o tamanho da estrutura de [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , em bytes.</span><span class="sxs-lookup"><span data-stu-id="67491-183">To finish initializing the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure, in bytes.</span></span>

<span data-ttu-id="67491-184">O exemplo a seguir retorna os componentes da URL na caixa de edição, IDC \_ PreOpen1 e retorna os componentes para a caixa de listagem, IDC \_ preopenlist.</span><span class="sxs-lookup"><span data-stu-id="67491-184">The following example returns the components of the URL in the edit box, IDC\_PreOpen1, and returns the components to the list box, IDC\_PreOpenList.</span></span> <span data-ttu-id="67491-185">Para exibir apenas as informações de um componente individual, essa função copia o caractere imediatamente após as informações do componente na cadeia de caracteres e o substitui temporariamente por um **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67491-185">To display only the information for an individual component, this function copies the character immediately after the component's information in the string and temporarily replaces it with a **NULL**.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a><span data-ttu-id="67491-186">Criando URLs</span><span class="sxs-lookup"><span data-stu-id="67491-186">Creating URLs</span></span>

<span data-ttu-id="67491-187">A função [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa as informações na estrutura [**de \_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) para criar um localizador de recursos uniforme.</span><span class="sxs-lookup"><span data-stu-id="67491-187">The [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) function uses the information in the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure to create a Uniform Resource Locator.</span></span>

<span data-ttu-id="67491-188">Os componentes que compõem a estrutura de [**\_ componentes de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) são o esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e informações adicionais (como parâmetros de pesquisa).</span><span class="sxs-lookup"><span data-stu-id="67491-188">The components that make up the [**URL\_COMPONENTS**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) structure are the scheme, host name, port number, user name, password, URL path, and additional information (such as search parameters).</span></span> <span data-ttu-id="67491-189">Cada componente, exceto o número da porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="67491-189">Each component, except the port number, has a string member that holds the information, and a member that holds the length of the string member.</span></span>

<span data-ttu-id="67491-190">Para cada componente necessário, o membro do ponteiro deve conter o endereço do buffer que contém as informações.</span><span class="sxs-lookup"><span data-stu-id="67491-190">For each required component, the pointer member should contain the address of the buffer holding the information.</span></span> <span data-ttu-id="67491-191">O membro de comprimento deve ser definido como zero se o membro do ponteiro contiver o endereço de uma cadeia de caracteres terminada em zero; o membro Length deve ser definido como o comprimento da cadeia de caracteres se o membro do ponteiro contiver o endereço de uma cadeia de caracteres que não seja terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="67491-191">The length member should be set to zero if the pointer member contains the address of a zero-terminated string; the length member should be set to the string length if the pointer member contains the address of a string that is not zero-terminated.</span></span> <span data-ttu-id="67491-192">O membro de ponteiro de quaisquer componentes que não são necessários deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="67491-192">The pointer member of any components that are not required must be **NULL**.</span></span>

## <a name="accessing-urls-directly"></a><span data-ttu-id="67491-193">Acessando URLs diretamente</span><span class="sxs-lookup"><span data-stu-id="67491-193">Accessing URLs Directly</span></span>

<span data-ttu-id="67491-194">Os recursos de FTP e HTTP na Internet podem ser acessados diretamente usando as funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="67491-194">FTP, and HTTP resources on the Internet can be accessed directly by using the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="67491-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) abre uma conexão com o recurso na URL passada para a função.</span><span class="sxs-lookup"><span data-stu-id="67491-195">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) opens a connection to the resource at the URL passed to the function.</span></span> <span data-ttu-id="67491-196">Quando essa conexão é feita, há duas etapas possíveis.</span><span class="sxs-lookup"><span data-stu-id="67491-196">When this connection is made, there are two possible steps.</span></span> <span data-ttu-id="67491-197">Primeiro, se o recurso for um arquivo, o [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) poderá baixá-lo; em segundo lugar, se o recurso for um diretório, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) poderá enumerar os arquivos dentro do diretório (exceto ao usar proxies de CERN).</span><span class="sxs-lookup"><span data-stu-id="67491-197">First, if the resource is a file, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can download it; second, if the resource is a directory, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) can enumerate the files within the directory (except when using CERN proxies).</span></span> <span data-ttu-id="67491-198">Para obter mais informações sobre o [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), consulte [lendo arquivos](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="67491-198">For more information on [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), see [Reading Files](common-functions.md).</span></span> <span data-ttu-id="67491-199">Para obter mais informações sobre o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consulte [localizando o próximo arquivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="67491-199">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="67491-200">Para aplicativos que precisam operar por meio de um proxy CERN, o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pode ser usado para acessar diretórios e arquivos FTP.</span><span class="sxs-lookup"><span data-stu-id="67491-200">For applications that need to operate through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used to access FTP directories and files.</span></span> <span data-ttu-id="67491-201">As solicitações de FTP são empacotadas para serem exibidas como uma solicitação HTTP, que o proxy do CERN aceitaria.</span><span class="sxs-lookup"><span data-stu-id="67491-201">The FTP requests are packaged to appear like an HTTP request, which the CERN proxy would accept.</span></span>

<span data-ttu-id="67491-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado pela função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e a URL do recurso.</span><span class="sxs-lookup"><span data-stu-id="67491-202">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function and the URL of the resource.</span></span> <span data-ttu-id="67491-203">A URL deve incluir o esquema (http:, FTP:, file: \[ para um arquivo local \] ou https: \[ for Hypertext Protocol Secure \] ) e o local de rede (como `www.microsoft.com` ).</span><span class="sxs-lookup"><span data-stu-id="67491-203">The URL must include the scheme (http:, ftp:, file: \[for a local file\], or https: \[for hypertext protocol secure\]) and network location (such as `www.microsoft.com`).</span></span> <span data-ttu-id="67491-204">A URL também pode incluir um caminho (por exemplo,/ISAPI/gomscom.asp? TARGET =/Windows/Feature/) e o nome do recurso (por exemplo, default.htm).</span><span class="sxs-lookup"><span data-stu-id="67491-204">The URL can also include a path (for example, /isapi/gomscom.asp?TARGET=/windows/feature/) and resource name (for example, default.htm).</span></span> <span data-ttu-id="67491-205">Para solicitações HTTP ou HTTPS, cabeçalhos adicionais podem ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="67491-205">For HTTP or HTTPS requests, additional headers can be included.</span></span>

<span data-ttu-id="67491-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (somente URLs http ou HTTPS) podem usar o identificador criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para baixar o recurso.</span><span class="sxs-lookup"><span data-stu-id="67491-206">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only) can use the handle that is created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to download the resource.</span></span>

<span data-ttu-id="67491-207">O diagrama a seguir ilustra quais identificadores usar com cada função.</span><span class="sxs-lookup"><span data-stu-id="67491-207">The following diagram illustrates which handles to use with each function.</span></span>

![identificadores a serem usados com funções](images/ax-wnt02.png)

<span data-ttu-id="67491-209">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raiz criado pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) é usado pelo [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="67491-209">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) is used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span> <span data-ttu-id="67491-210">O identificador **HINTERNET** criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pode ser usado por [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (não mostrado aqui) e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (somente URLs http ou HTTPS).</span><span class="sxs-lookup"><span data-stu-id="67491-210">The **HINTERNET** handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) can be used by [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (not shown here), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP or HTTPS URLs only).</span></span>

<span data-ttu-id="67491-211">Para obter mais informações, consulte [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="67491-211">For more information, see [**HINTERNET Handles**](appendix-a-hinternet-handles.md).</span></span>

> [!Note]  
> <span data-ttu-id="67491-212">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="67491-212">WinINet does not support server implementations.</span></span> <span data-ttu-id="67491-213">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="67491-213">In addition, it should not be used from a service.</span></span> <span data-ttu-id="67491-214">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="67491-214">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 