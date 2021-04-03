---
title: Localizando sistemas de host de servidor
description: Localizando sistemas de host de servidor usando associações de cadeia de caracteres e consultando um banco de dados de serviço de nome para o local de um programa de servidor.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822709"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="bc6b8-103">Localizando sistemas de host de servidor</span><span class="sxs-lookup"><span data-stu-id="bc6b8-103">Finding Server Host Systems</span></span>

<span data-ttu-id="bc6b8-104">Um sistema host do servidor é o computador que executa o programa do servidor do aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="bc6b8-105">Pode haver um ou vários sistemas de host de servidor em uma rede.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="bc6b8-106">A forma como o programa cliente encontra um servidor para se conectar depende das necessidades do seu programa.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="bc6b8-107">Há dois métodos para localizar sistemas de host de servidor:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="bc6b8-108">Usar informações armazenadas em cadeias de caracteres no código-fonte do cliente, variáveis de ambiente ou arquivos de configuração específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="bc6b8-109">O aplicativo cliente pode usar os dados na cadeia de caracteres para compor uma associação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="bc6b8-110">Consultando um banco de dados de serviço de nome para o local de um programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="bc6b8-111">Esta seção apresenta informações sobre essas duas técnicas nos tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="bc6b8-112">Usando associações de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="bc6b8-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="bc6b8-113">Importando de bancos de dados de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="bc6b8-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="bc6b8-114">Usando associações de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="bc6b8-114">Using String Bindings</span></span>

<span data-ttu-id="bc6b8-115">Os aplicativos podem criar associações de informações armazenadas em cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="bc6b8-116">O aplicativo cliente compõe essas informações como uma cadeia de caracteres e, em seguida, chama a função [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) .</span><span class="sxs-lookup"><span data-stu-id="bc6b8-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="bc6b8-117">O cliente deve fornecer as seguintes informações para identificar o servidor:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="bc6b8-118">O nome da interface, o GUID (identificador global exclusivo) do objeto ou UUID do objeto.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="bc6b8-119">Para obter mais informações, consulte [gerando UUIDs de interface](generating-interface-uuids.md) e [UUID de cadeia de caracteres](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="bc6b8-120">O tipo de transporte para se comunicar, como pipes nomeados ou TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="bc6b8-121">Para obter detalhes, consulte [terminologia de ligação de RPC essencial](essential-rpc-binding-terminology.md) e [selecionando uma sequência de protocolo](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="bc6b8-122">O endereço de rede ou o nome do computador host do servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="bc6b8-123">O ponto de extremidade do programa de servidor no computador host do servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="bc6b8-124">Para obter mais informações, consulte [localizando pontos de extremidade](finding-endpoints.md)e [especificando pontos de extremidade](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="bc6b8-125">(O UUID do objeto e as informações do ponto de extremidade são opcionais.)</span><span class="sxs-lookup"><span data-stu-id="bc6b8-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="bc6b8-126">Nos exemplos a seguir, o parâmetro *pszNetworkAddress* e outros parâmetros incluem barras invertidas incorporadas.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="bc6b8-127">A barra invertida é um caractere de escape na linguagem de programação C.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="bc6b8-128">Duas barras invertidas são necessárias para representar cada caractere de barra invertida literal único.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="bc6b8-129">A estrutura de associação de cadeia de caracteres deve conter quatro caracteres de barra invertida para representar os dois caracteres de barra invertida literal que precedem o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="bc6b8-130">O exemplo a seguir mostra que o nome do servidor deve ser precedido por oito barras invertidas para que quatro caracteres de barra invertida literal apareçam na estrutura de dados de vinculação de cadeia de caracteres depois que a função **sprintf \_ s** processa a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="bc6b8-131">No exemplo a seguir, a associação de cadeia de caracteres aparece como:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="bc6b8-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *nomeservidor* \[ \\ \\ \\ \\  pipe pipeName\]</span><span class="sxs-lookup"><span data-stu-id="bc6b8-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="bc6b8-133">Em seguida, o cliente chama [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obter o identificador de associação:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="bc6b8-134">Uma função de conveniência, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) , monta o UUID do objeto, a sequência de protocolos, o endereço de rede e o ponto de extremidade na sintaxe correta para a chamada para [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="bc6b8-135">Você não precisa se preocupar em colocar o e comercial, dois-pontos e os vários componentes para cada sequência de protocolo no local certo; Você apenas fornece as cadeias de caracteres como parâmetros para a função.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="bc6b8-136">A biblioteca de tempo de execução mesmo aloca a memória necessária para a associação de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="bc6b8-137">Outra função de conveniência, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), usa um identificador de associação como entrada e produz a associação de cadeia de caracteres correspondente.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="bc6b8-138">Importando de bancos de dados de serviço de nome</span><span class="sxs-lookup"><span data-stu-id="bc6b8-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="bc6b8-139">Os bancos de dados do serviço de nome armazenam, entre outras coisas, identificadores e UUIDs de associação.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="bc6b8-140">O aplicativo cliente pode procurar um ou ambos quando precisar fazer a ligação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="bc6b8-141">Para obter uma discussão sobre as informações que um serviço de nome armazena e o formato de armazenamento, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="bc6b8-142">A Biblioteca RPC fornece dois conjuntos de funções que seu programa cliente pode usar para pesquisar o banco de dados do serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="bc6b8-143">Os nomes de um conjunto começam com RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="bc6b8-144">Os nomes do outro conjunto começam com RpcNsBindingLookup.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="bc6b8-145">A diferença entre os dois grupos de funções é que as funções RpcNsBindingImport retornam um único identificador de associação por chamada e as funções RpcNsBindingLookup retornam grupos de identificadores por chamada.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="bc6b8-146">Para iniciar uma pesquisa com as funções RpcNsBindingImport, primeiro chame [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), conforme mostrado no fragmento de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="bc6b8-147">Quando as funções RPC pesquisam o banco de dados do serviço de nome, elas precisam de um local para iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="bc6b8-148">Na terminologia de RPC, isso é chamado de nome de entrada.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="bc6b8-149">O programa cliente passa o nome da entrada como o segundo parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="bc6b8-150">Esse parâmetro poderá ser **nulo** se você quiser pesquisar todo o banco de dados do serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="bc6b8-151">Como alternativa, você pode pesquisar a entrada de servidor passando um nome de entrada de servidor ou pesquisar a entrada de grupo passando um nome de entrada de grupo.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="bc6b8-152">Passar um nome de entrada restringe a pesquisa para o conteúdo dessa entrada.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="bc6b8-153">No exemplo anterior, o valor padrão da \_ sintaxe RPC C \_ ns \_ \_ é passado como o primeiro parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="bc6b8-154">Isso seleciona a sintaxe de nome de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="bc6b8-155">Atualmente, essa é a única sintaxe de nome de entrada com suporte.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="bc6b8-156">Seu aplicativo cliente pode pesquisar o nome do banco de dados do serviço de nome de uma interface, um UUID ou ambos.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="bc6b8-157">Se você quiser que ele pesquise uma interface por nome, passe a variável de interface global que o compilador MIDL gera de seu arquivo IDL como o terceiro parâmetro para [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="bc6b8-158">Você encontrará sua declaração no arquivo de cabeçalho que o compilador MIDL gerou quando gerou o stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="bc6b8-159">Se você quiser que o programa cliente pesquise por UUID somente, defina o terceiro parâmetro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="bc6b8-160">Ao pesquisar o banco de dados do serviço de nome para um UUID, defina o quarto parâmetro de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) como o UUID que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="bc6b8-161">Se você não estiver procurando um UUID, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="bc6b8-162">A função [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa o endereço de um serviço de nome – identificador de contexto de pesquisa por meio de seu quinto parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="bc6b8-163">Você passa esse parâmetro para outras funções RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="bc6b8-164">Em particular, a próxima função que seu aplicativo cliente chamaria é [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="bc6b8-165">Os programas cliente usam essa função para recuperar identificadores de associação compatíveis do banco de dados do serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="bc6b8-166">O fragmento de código a seguir demonstra como essa função pode ser chamada:</span><span class="sxs-lookup"><span data-stu-id="bc6b8-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="bc6b8-167">Depois de chamar a função [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obter um identificador de associação, o aplicativo cliente pode determinar se o identificador recebido é aceitável.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="bc6b8-168">Caso contrário, o programa cliente pode executar um loop e chamar **RpcNsBindingImportNext** novamente para ver se o serviço de nome contém um identificador mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="bc6b8-169">Para cada chamada para **RpcNsBindingImportNext**, deve haver uma chamada correspondente para RpcNsBindingFree.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="bc6b8-170">Quando a pesquisa for concluída, chame a função [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar o contexto de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="bc6b8-171">Depois que o aplicativo cliente tem um identificador de associação aceitável, ele deve verificar se o aplicativo do servidor está em execução.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="bc6b8-172">Há dois métodos que o cliente pode usar para executar essa verificação.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="bc6b8-173">A primeira é chamar uma função na interface do cliente.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="bc6b8-174">Se o programa do servidor estiver em execução, a chamada será concluída.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="bc6b8-175">Caso contrário, a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="bc6b8-175">If not, the call will fail.</span></span> <span data-ttu-id="bc6b8-176">Uma maneira melhor de verificar se o servidor está em execução é invocar [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguido de uma chamada para [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="bc6b8-177">Para obter mais informações sobre o nome de banco de dados do serviço, consulte [o banco de dados do serviço de nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b8-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




