---
title: Ferramenta de compilador de serviço Web
description: Para dar suporte ao modelo de serviço, wsutil.exe gera o cabeçalho a ser usado no lado do cliente e do serviço. Ele gera o arquivo de proxy C para o lado do cliente e o arquivo stub C para o lado do serviço, conforme necessário.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Serviços Web da ferramenta de compilador de serviço Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368953"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="7cbe1-107">Ferramenta de compilador de serviço Web</span><span class="sxs-lookup"><span data-stu-id="7cbe1-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="7cbe1-108">Para dar suporte ao modelo de serviço, wsutil.exe gera o cabeçalho a ser usado no lado do cliente e do serviço.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="7cbe1-109">Ele gera o arquivo de proxy C para o lado do cliente e o arquivo stub C para o lado do serviço, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="7cbe1-110">Para dar suporte à [serialização](serialization.md), o compilador gera cabeçalhos para descrições de elemento para definições de elementos globais e todas as informações de definição de tipo no arquivo de proxy a serem consumidas pelo mecanismo de serialização.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="7cbe1-111">Uso</span><span class="sxs-lookup"><span data-stu-id="7cbe1-111">Usage</span></span>

<span data-ttu-id="7cbe1-112">**Opções de opção de linha de comando deWsUtil.exe \[ \[ \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="7cbe1-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="7cbe1-113">opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="7cbe1-113">command-line-switches</span></span>

<span data-ttu-id="7cbe1-114">Especifica WsUtil.exe opções do compilador.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="7cbe1-115">As opções podem aparecer em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-115">Switches can appear in any order.</span></span> <span data-ttu-id="7cbe1-116">Dash ('-') e barra ('/') são tratados como o mesmo.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="7cbe1-117">Lista de opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="7cbe1-117">List of command line options</span></span>

-   <span data-ttu-id="7cbe1-118">@filename Especifica que o arquivo de entrada deve ser tratado como um arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="7cbe1-119">Essa opção pode ser usada várias vezes, em qualquer lugar na lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="7cbe1-120">/WSDL: <filename> : <\_ url opcional> especifica que o arquivo de entrada deve ser tratado como um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="7cbe1-121">Várias entradas WSDL são permitidas e todos os arquivos WSDL especificados são processados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="7cbe1-122">A \_ URL opcional especifica o local do qual os metadados foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="7cbe1-123">Se nenhuma \_ URL opcional for especificada, Wsutil gerará uma URL exclusiva internamente.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="7cbe1-124">Consulte também [suporte a políticas](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="7cbe1-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="7cbe1-125">/xsd: <filename> especifica que o nome de arquivo de entrada deve ser tratado como um arquivo de esquema.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="7cbe1-126">Várias entradas XSD são permitidas e todos os arquivos de esquema especificados são processados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="7cbe1-127">/WSP: <filename> : <\_ url opcional> especifica que o nome de arquivo de entrada deve ser tratado como metadados de política.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="7cbe1-128">Várias entradas WSP são permitidas e todos os arquivos de política especificados são processados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="7cbe1-129">A \_ URL opcional especifica o local do qual os metadados foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="7cbe1-130">Se nenhuma \_ URL opcional for especificada, Wsutil gerará uma URL exclusiva internamente.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="7cbe1-131">Os arquivos de política serão ignorados se o sinalizador/nopolicy for especificado.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="7cbe1-132">Consulte também [suporte a políticas](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="7cbe1-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="7cbe1-133">/nopolicy desabilitar o processamento de política.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="7cbe1-134">/out: <dirname> especifica o nome do diretório para arquivos de saída</span><span class="sxs-lookup"><span data-stu-id="7cbe1-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="7cbe1-135">/noclient não geram o stub do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="7cbe1-136">/noservice não geram o stub do lado do serviço.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="7cbe1-137">/prefix: <string> preceder a cadeia de caracteres especificada para todos os identificadores gerados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="7cbe1-138">/FullName preceda o nome de arquivo normalizado para identificadores gerados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="7cbe1-139">Por padrão, somente o nome especificado no atributo "Name" será usado para gerar identificadores para descrições relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="7cbe1-140">/String: <WS \_ string>\|<WCHAR \*> por padrão, Wsutil gera WCHAR \* para o tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="7cbe1-141">O aplicativo pode usar esse sinalizador para substituir esse comportamento e gera a \_ cadeia de caracteres WS para xsd: Type.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="7cbe1-142">/Help exibir mensagem de ajuda</span><span class="sxs-lookup"><span data-stu-id="7cbe1-142">/help Display help message</span></span>
-   <span data-ttu-id="7cbe1-143">/?</span><span class="sxs-lookup"><span data-stu-id="7cbe1-143">/?</span></span> <span data-ttu-id="7cbe1-144">Mesmo que/Help</span><span class="sxs-lookup"><span data-stu-id="7cbe1-144">Same as /help</span></span>
-   <span data-ttu-id="7cbe1-145">/W: x opções de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-145">/W:x Error handling options.</span></span> <span data-ttu-id="7cbe1-146">Poderia ser W:0-W: 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="7cbe1-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="7cbe1-147">/nologo não gere informações específicas do compilador na saída do console.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="7cbe1-148">/nostamp não gere informações específicas do compilador em arquivos gerados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="7cbe1-149">Por padrão, o compilador gera os seguintes arquivos para o arquivo WSDL ou o WSDL retornado da troca de metadados:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="7cbe1-150">Proxy do cliente ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7cbe1-151">Stub de serviço ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7cbe1-152">Arquivo de cabeçalho ({inputfilename}. h)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="7cbe1-153">A raiz do filename gerado é o nome do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="7cbe1-154">As extensões de arquivo de entrada originais são preservadas para evitar a colisão de nome de arquivo para arquivos gerados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="7cbe1-155">Por padrão, os stubs de serviço e cliente são gerados no mesmo arquivo, com o código stub de serviço gerado após o código de proxy.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="7cbe1-156">Por padrão, o compilador gera os seguintes arquivos para um arquivo XSD para o esquema retornado da troca de metadados:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="7cbe1-157">descrições de serialização ({inputfilename}. c)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="7cbe1-158">Arquivo de cabeçalho ({inputfilename}. h)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="7cbe1-159">A raiz do nome do arquivo é o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="7cbe1-160">Wsutil.exe gera uma seção "Stamp" no início de todos os arquivos gerados, indicando a opção do compilador, a versão da ferramenta, a opção de linha de comando aplicável, etc. Esta seção pode ser desativada usando a opção/nostamp para evitar ruídos com a comparação de arquivos gerados.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="7cbe1-161">Wsutil não dá suporte ao download de metadados</span><span class="sxs-lookup"><span data-stu-id="7cbe1-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="7cbe1-162">O compilador Wsutil funciona somente do arquivo de metadados local.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="7cbe1-163">A ferramenta não oferece suporte ao download de metadados de serviços Web em execução.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="7cbe1-164">Os desenvolvedores podem usar outras ferramentas WebService com suporte, como SvcUtil, para baixar metadados para o computador local, inspecionar os arquivos salvos e passar esses arquivos para wsutil.exe para compilação.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="7cbe1-165">Suporte a vários arquivos de entrada/saída</span><span class="sxs-lookup"><span data-stu-id="7cbe1-165">Multiple input/output file support</span></span>

<span data-ttu-id="7cbe1-166">O esquema WSDL e XML permite incluir/importar definições de outros espaços de nome especificados em outros locais/arquivos.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="7cbe1-167">O Wsutil dá suporte a várias entradas de esquema/WSDL/política e gera um conjunto de stub/cabeçalho para cada arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="7cbe1-168">O Wsutil não segue as instruções include e Import.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="7cbe1-169">Em vez disso, o aplicativo deve passar arquivos que contenham todos os namespaces necessários para Wsutil, de modo que a ferramenta possa resolver todas as dependências durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="7cbe1-170">**WsUtil.exe/xsd: StockQuote. XSD/WSDL: StockQuote. WSDL/WSDL: StockQuoteService. WSDL**</span><span class="sxs-lookup"><span data-stu-id="7cbe1-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="7cbe1-171">o Wsutil gera três conjuntos de arquivos de saída:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="7cbe1-172">StockQuote. xsd. c StockQuote. xsd. h</span><span class="sxs-lookup"><span data-stu-id="7cbe1-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="7cbe1-173">StockQuote. WSDL. c StockQuote. WSDL. h</span><span class="sxs-lookup"><span data-stu-id="7cbe1-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="7cbe1-174">StockQuoteService. WSDL. h stockquoteservices. WSDL. c</span><span class="sxs-lookup"><span data-stu-id="7cbe1-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="7cbe1-175">Formato do arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="7cbe1-175">Output file format</span></span>

<span data-ttu-id="7cbe1-176">Para cada arquivo de saída, o Wsutil gera definições externas disponíveis no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="7cbe1-177">Além de definições de estrutura C e protótipos de função de stub, todas as outras definições relacionadas a serviços Web são encapsuladas em uma estrutura global chamada com nome de arquivo normalizado.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="7cbe1-178">Observe que nem todos os campos são gerados para a estrutura global.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="7cbe1-179">Um campo de nível superior é gerado somente quando as definições relacionadas são especificadas no arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="7cbe1-180">Por exemplo, nenhum campo de mensagem, operações e contratos é gerado para arquivos XSD.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="7cbe1-181">Níveis de aviso e nível de erro</span><span class="sxs-lookup"><span data-stu-id="7cbe1-181">Warning Levels and error level</span></span>

<span data-ttu-id="7cbe1-182">Semelhante ao compilador C, o WsUtil.exe dá suporte a quatro níveis de aviso e um nível de erro:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="7cbe1-183">WsUtil.exe gera erros com falhas irrecuperáveis, como arquivo WSDL inválido, opções de compilador inválidas etc.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="7cbe1-184">O WsUtil gera avisos de W1 com sérios problemas recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="7cbe1-185">O compilador pode continuar, mas o usuário deve estar ciente do problema.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="7cbe1-186">Por exemplo, um aviso de W1 será gerado se houver atributos sem suporte, como algumas facetas WSDL, em WSDL que não afetam a geração de código.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="7cbe1-187">O WsUtil gera avisos de W2 com problemas menos graves.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="7cbe1-188">Não há perda de funcionalidade, mas o desenvolvedor de aplicativos pode querer saber isso.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="7cbe1-189">Como comportamentos que podem ser diferentes de outras plataformas.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="7cbe1-190">O WsUtil gera avisos w3 com impacto mínimo sobre o código gerado.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="7cbe1-191">Por exemplo, wsutil.exe gera um aviso w3 quando a cadeia de caracteres normalizada é diferente da cadeia de caracteres original.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="7cbe1-192">O erro de W4 é mais semelhante aos avisos "informativos" e WsUtil o W4, em casos como ignorar o atributo de documentação no WSDL.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="7cbe1-193">O WX indica que o compilador trata o aviso como erro.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="7cbe1-194">Por exemplo, Wsutil gerará um erro para todos os avisos de W1 se/W: 1/WX for especificado.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="7cbe1-195">/W: {N} especifique qual nível de mensagem de aviso deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="7cbe1-196">/W: 1 significa que os avisos do nível de aviso 1 devem ser gerados e os avisos do nível de aviso 2 e inferior devem ser mascarados e não gerados pela ferramenta.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="7cbe1-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="7cbe1-197">/fullname</span></span>

<span data-ttu-id="7cbe1-198">Essa opção indica que WsUtil.exe gera um nome completo para identificadores para evitar a possível colisão de nomes.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="7cbe1-199">Por exemplo, no example. xsd temos:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="7cbe1-200">Por padrão, o WsUtil.exe gera:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="7cbe1-201">Mas se a opção de linha de comando/FullName for especificada, WsUtil.exe gerará a seguinte definição de estrutura em vez disso:</span><span class="sxs-lookup"><span data-stu-id="7cbe1-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="7cbe1-202">Globalização</span><span class="sxs-lookup"><span data-stu-id="7cbe1-202">Globalization</span></span>

<span data-ttu-id="7cbe1-203">A ferramenta é neutra de idioma e pode ser localizada em idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="7cbe1-204">Todas as mensagens de erro/saída do console podem ser localizadas.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="7cbe1-205">No entanto, as opções de linha de comando permanecem em inglês.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="7cbe1-206">Variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="7cbe1-206">Environment Variable</span></span>

<span data-ttu-id="7cbe1-207">WsUtil.exe não usa nenhuma variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="7cbe1-208">Independente de plataforma</span><span class="sxs-lookup"><span data-stu-id="7cbe1-208">Platform independent</span></span>

<span data-ttu-id="7cbe1-209">Os arquivos de saída de WsUtil.exe são independentes de plataforma.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="7cbe1-210">Não há código dependente de arquitetura gerado no stub; qualquer outra arquitetura específica será encarregada pelo compilador do C.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="7cbe1-211">O stub pode ser usado em todas as plataformas às quais damos suporte.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="7cbe1-212">A descrição de wsutil.exe saída pode ser encontrada em [suporte WSDL](wsdl-support.md) e parte de [suporte do esquema](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="7cbe1-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 




