---
title: Configurando e recuperando opções da Internet
description: Este tópico descreve como definir e recuperar opções da Internet usando as funções InternetSetOption e InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Configurando e recuperando opções da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823922"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="f0dba-104">Configurando e recuperando opções da Internet</span><span class="sxs-lookup"><span data-stu-id="f0dba-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="f0dba-105">Este tópico descreve como definir e recuperar opções da Internet usando as funções [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="f0dba-106">As opções da Internet podem ser definidas em ou recuperadas de um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado ou as configurações atuais no Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f0dba-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="f0dba-107">Etapas de implementação</span><span class="sxs-lookup"><span data-stu-id="f0dba-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="f0dba-108">Escolhendo Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="f0dba-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="f0dba-109">Escolhendo o identificador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="f0dba-110">Configurando ou recuperando as opções</span><span class="sxs-lookup"><span data-stu-id="f0dba-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="f0dba-111">Escopo do identificador de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="f0dba-112">Definindo opções individuais</span><span class="sxs-lookup"><span data-stu-id="f0dba-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="f0dba-113">Recuperando opções individuais</span><span class="sxs-lookup"><span data-stu-id="f0dba-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="f0dba-114">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="f0dba-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="f0dba-115">Definindo opções de conexão</span><span class="sxs-lookup"><span data-stu-id="f0dba-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="f0dba-116">Recuperando opções de conexão</span><span class="sxs-lookup"><span data-stu-id="f0dba-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="f0dba-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0dba-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="f0dba-118">Etapas de implementação</span><span class="sxs-lookup"><span data-stu-id="f0dba-118">Implementation Steps</span></span>

<span data-ttu-id="f0dba-119">Para definir ou recuperar as opções da Internet, conclua o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f0dba-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="f0dba-120">Escolhendo Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="f0dba-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="f0dba-121">Escolhendo o identificador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="f0dba-122">Configurando ou recuperando as opções</span><span class="sxs-lookup"><span data-stu-id="f0dba-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="f0dba-123">Escolhendo Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="f0dba-123">Choosing Internet Options</span></span>

<span data-ttu-id="f0dba-124">Como há tantas opções da Internet, a escolha das opções corretas é importante.</span><span class="sxs-lookup"><span data-stu-id="f0dba-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="f0dba-125">Muitas opções da Internet afetam o comportamento das funções WinINet e do Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="f0dba-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="f0dba-126">Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="f0dba-126">For example, you can:</span></span>

-   <span data-ttu-id="f0dba-127">Manipule a autenticação básica de servidor e proxy definindo nomes de usuário e senhas.</span><span class="sxs-lookup"><span data-stu-id="f0dba-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="f0dba-128">Defina ou recupere a cadeia de caracteres do agente do usuário usada pelos servidores para identificar os recursos do aplicativo cliente ou do navegador.</span><span class="sxs-lookup"><span data-stu-id="f0dba-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="f0dba-129">Recupere o tipo de identificador do identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="f0dba-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="f0dba-130">Para obter mais informações e uma lista das opções da Internet, consulte [**sinalizadores de opção**](option-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f0dba-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="f0dba-131">No Internet Explorer 5 e posterior, algumas opções podem ser definidas ou recuperadas de uma conexão de Internet específica usando a lista de opções [**Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) e as estruturas de [**opção de Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="f0dba-132">Para obter mais informações e uma lista de opções que podem ser definidas ou recuperadas de uma conexão de Internet específica, consulte o membro **dwOptions** da estrutura da [**\_ opção Internet por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="f0dba-133">Escolhendo o identificador HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="f0dba-134">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) usado para definir ou recuperar as opções da Internet determina o escopo da operação.</span><span class="sxs-lookup"><span data-stu-id="f0dba-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="f0dba-135">Todos os identificadores criados por meio desse identificador herdarão as opções definidas nesse identificador.</span><span class="sxs-lookup"><span data-stu-id="f0dba-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="f0dba-136">Por exemplo, aplicativos cliente que exigem um proxy com autenticação, provavelmente não exigem a configuração do nome de usuário e da senha do proxy sempre que o aplicativo tentar acessar um recurso da Internet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="f0dba-137">Se todas as solicitações em uma determinada conexão forem tratadas pelo mesmo proxy, definir o nome de usuário e a senha do proxy em um tipo de conexão [**HINTERNET**](appendix-a-hinternet-handles.md) identificador, ou seja, um identificador criado por uma chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permitiria que qualquer chamada derivada desse identificador **HINTERNET** use o mesmo nome de usuário e senha do proxy.</span><span class="sxs-lookup"><span data-stu-id="f0dba-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="f0dba-138">Definir o nome de usuário e a senha do proxy sempre que um identificador de **HINTERNET** é criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) exigiria sobrecarga extra e desnecessária.</span><span class="sxs-lookup"><span data-stu-id="f0dba-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="f0dba-139">Lembre-se de que, se o aplicativo usar um proxy que requer autenticação, ele deverá definir as credenciais de proxy em cada nova conexão.</span><span class="sxs-lookup"><span data-stu-id="f0dba-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="f0dba-140">Configurando ou recuperando as opções</span><span class="sxs-lookup"><span data-stu-id="f0dba-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="f0dba-141">Quando você tiver determinado o que as opções da Internet e o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para usar, recupere essas opções da Internet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="f0dba-142">Para definir ou recuperar opções, chame [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="f0dba-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="f0dba-143">Escopo do identificador de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="f0dba-144">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) usado para definir ou recuperar as opções da Internet determina as ações para as quais as opções são válidas.</span><span class="sxs-lookup"><span data-stu-id="f0dba-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="f0dba-145">Esses identificadores têm três níveis:</span><span class="sxs-lookup"><span data-stu-id="f0dba-145">These handles have three levels:</span></span>

-   <span data-ttu-id="f0dba-146">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raiz (criado por uma chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) conterá todas as opções da Internet que afetam essa instância do Wininet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="f0dba-147">[**HINTERNET**](appendix-a-hinternet-handles.md) identificadores que se conectam a um servidor (criado por uma chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span><span class="sxs-lookup"><span data-stu-id="f0dba-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="f0dba-148">Identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) associados a um recurso ou enumeração de recursos em um servidor específico.</span><span class="sxs-lookup"><span data-stu-id="f0dba-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="f0dba-149">Além dos vários identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , um aplicativo também pode usar **NULL** para definir ou recuperar os valores padrão das opções da Internet usadas pelo Internet Explorer e as funções do Wininet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="f0dba-150">Definir opções da Internet ao usar **NULL** como o identificador altera os valores padrão das opções, que atualmente estão armazenadas no registro.</span><span class="sxs-lookup"><span data-stu-id="f0dba-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="f0dba-151">Os aplicativos cliente não devem usar funções de registro para alterar os valores padrão das opções da Internet, pois a implementação de como as opções são armazenadas pode ser alterada no futuro.</span><span class="sxs-lookup"><span data-stu-id="f0dba-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="f0dba-152">A tabela a seguir lista o tipo de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) e o escopo das opções da Internet associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="f0dba-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0dba-153">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="f0dba-153">Handle Type</span></span></th>
<th><span data-ttu-id="f0dba-154">Escopo</span><span class="sxs-lookup"><span data-stu-id="f0dba-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0dba-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="f0dba-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="f0dba-156">As configurações de opção padrão para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f0dba-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="f0dba-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="f0dba-158">As configurações de opção para essa conexão com um servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="f0dba-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="f0dba-159">Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0dba-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="f0dba-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="f0dba-161">As configurações de opção para essa conexão com um servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="f0dba-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="f0dba-162">Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0dba-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0dba-163">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0dba-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="f0dba-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="f0dba-165">As configurações de opção para essa conexão com um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0dba-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="f0dba-166">Essas opções afetam as operações iniciadas a partir desse identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como downloads de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0dba-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="f0dba-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="f0dba-168">As configurações de opção associadas a essa solicitação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0dba-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="f0dba-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="f0dba-170">As configurações de opção associadas a este download de recurso de FTP.</span><span class="sxs-lookup"><span data-stu-id="f0dba-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="f0dba-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="f0dba-172">As configurações de opção associadas a este download de recurso de FTP são formatadas em HTML.</span><span class="sxs-lookup"><span data-stu-id="f0dba-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="f0dba-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="f0dba-174">As configurações de opção associadas a esta pesquisa de arquivos em um servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="f0dba-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="f0dba-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="f0dba-176">As configurações de opção associadas a esta pesquisa de arquivos em um servidor FTP formatado em HTML.</span><span class="sxs-lookup"><span data-stu-id="f0dba-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="f0dba-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="f0dba-178">As configurações de opção associadas a este download de recurso do Gopher.</span><span class="sxs-lookup"><span data-stu-id="f0dba-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0dba-179">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0dba-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="f0dba-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="f0dba-181">As configurações de opção associadas a este download de recurso do Gopher são formatadas em HTML.</span><span class="sxs-lookup"><span data-stu-id="f0dba-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0dba-182">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0dba-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="f0dba-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="f0dba-184">As configurações de opção associadas a esta pesquisa de arquivos em um servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="f0dba-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0dba-185">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0dba-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="f0dba-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="f0dba-187">As configurações de opção associadas a esta pesquisa de arquivos em um servidor gopher formatado em HTML.</span><span class="sxs-lookup"><span data-stu-id="f0dba-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0dba-188">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f0dba-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0dba-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="f0dba-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="f0dba-190">As configurações de opção associadas a essa solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f0dba-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0dba-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="f0dba-192">As configurações de opção associadas a esta instância das funções WinINet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="f0dba-193">Definindo opções individuais</span><span class="sxs-lookup"><span data-stu-id="f0dba-193">Setting Individual Options</span></span>

<span data-ttu-id="f0dba-194">Depois de determinar as opções da Internet que você deseja definir e o escopo que você deseja que sejam afetados por essas opções, a definição de opções da Internet não é complicada.</span><span class="sxs-lookup"><span data-stu-id="f0dba-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="f0dba-195">Tudo o que você precisa fazer é chamar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) desejado, o sinalizador de opção da Internet e um buffer que contém as informações que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="f0dba-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="f0dba-196">O exemplo a seguir mostra como definir o nome de usuário e a senha do proxy em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="f0dba-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="f0dba-197">Recuperando opções individuais</span><span class="sxs-lookup"><span data-stu-id="f0dba-197">Retrieving Individual Options</span></span>

<span data-ttu-id="f0dba-198">As opções da Internet podem ser recuperadas usando a função [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="f0dba-199">Para recuperar as opções da Internet:</span><span class="sxs-lookup"><span data-stu-id="f0dba-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="f0dba-200">Determine o tamanho do buffer necessário para recuperar as informações da opção da Internet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="f0dba-201">O tamanho do buffer pode ser determinado usando **NULL** para o endereço do buffer e passando um tamanho de buffer igual a zero.</span><span class="sxs-lookup"><span data-stu-id="f0dba-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="f0dba-202">O valor retornado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) é a quantidade de memória necessária para recuperar as informações, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f0dba-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="f0dba-203">Aloque uma memória para o buffer.</span><span class="sxs-lookup"><span data-stu-id="f0dba-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="f0dba-204">Recupere os dados.</span><span class="sxs-lookup"><span data-stu-id="f0dba-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="f0dba-205">Libere a memória.</span><span class="sxs-lookup"><span data-stu-id="f0dba-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="f0dba-206">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="f0dba-206">Complete Sample</span></span>

<span data-ttu-id="f0dba-207">Veja a seguir o exemplo completo usado na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="f0dba-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="f0dba-208">Este exemplo mostra como recuperar a cadeia de caracteres do agente do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="f0dba-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="f0dba-209">Definindo opções de conexão</span><span class="sxs-lookup"><span data-stu-id="f0dba-209">Setting Connection Options</span></span>

<span data-ttu-id="f0dba-210">No Internet Explorer 5 e posterior, as opções da Internet podem ser definidas para em uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="f0dba-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="f0dba-211">Anteriormente, todas as conexões compartilharam as mesmas configurações de opção de Internet.</span><span class="sxs-lookup"><span data-stu-id="f0dba-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="f0dba-212">Para definir opções para uma conexão específica:</span><span class="sxs-lookup"><span data-stu-id="f0dba-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="f0dba-213">Crie uma estrutura de [**lista de opções de Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="f0dba-214">Aloque a memória para as opções individuais da Internet que você deseja definir para a conexão.</span><span class="sxs-lookup"><span data-stu-id="f0dba-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="f0dba-215">Defina as opções em estruturas de [**opção de Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="f0dba-216">Defina as opções usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="f0dba-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="f0dba-217">O exemplo de código a seguir mostra como definir dados de proxy para uma conexão de LAN.</span><span class="sxs-lookup"><span data-stu-id="f0dba-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="f0dba-218">Recuperando opções de conexão</span><span class="sxs-lookup"><span data-stu-id="f0dba-218">Retrieving Connection Options</span></span>

<span data-ttu-id="f0dba-219">No Internet Explorer 5 e posterior, as opções da Internet podem ser recuperadas de uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="f0dba-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="f0dba-220">Para recuperar opções de uma conexão específica:</span><span class="sxs-lookup"><span data-stu-id="f0dba-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="f0dba-221">Crie uma estrutura de [**lista de opções de Internet \_ por \_ \_ \_ Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="f0dba-222">Aloque a memória para as opções individuais da Internet a serem recuperadas da conexão.</span><span class="sxs-lookup"><span data-stu-id="f0dba-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="f0dba-223">Especifique as opções usando as estruturas de [**opção da Internet \_ por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="f0dba-224">Recupere as opções usando [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="f0dba-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="f0dba-225">Utilize os dados da opção.</span><span class="sxs-lookup"><span data-stu-id="f0dba-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="f0dba-226">Libere a memória, alocada para conter os dados da opção, usando a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="f0dba-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="f0dba-227">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="f0dba-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="f0dba-228">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="f0dba-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f0dba-229">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f0dba-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f0dba-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0dba-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0dba-231">Manipulando a autenticação</span><span class="sxs-lookup"><span data-stu-id="f0dba-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="f0dba-232">Identificadores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="f0dba-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

