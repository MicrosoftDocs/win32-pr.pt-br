---
description: Ao acessar um servidor de Instrumentação de Gerenciamento do Windows (WMI) com um script, você pode escolher entre os protocolos de autenticação do NT LAN Manager (NTLM) ou Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Configurando o serviço de autenticação usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771647"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="bdbbe-103">Configurando o serviço de autenticação usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="bdbbe-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="bdbbe-104">Ao acessar um servidor de Instrumentação de Gerenciamento do Windows (WMI) com um script, você pode escolher entre os protocolos de autenticação do NT LAN Manager (NTLM) ou Kerberos.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="bdbbe-105">Não é necessário especificar o Kerberos, exceto ao usar a delegação.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="bdbbe-106">Para obter mais informações, consulte [conectando-se a um terceiro computador-delegação](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="bdbbe-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="bdbbe-107">Como as versões do sistema operacional diferem em qual serviço de autenticação eles usam, é recomendável que você não especifique um valor para o campo autoridade ao se conectar a um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="bdbbe-108">Em vez disso, permita que o sistema operacional e a versão distribuída do Component Object Model (DCOM) selecionem NTLM ou Kerberos.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="bdbbe-109">Se um serviço de autenticação for especificado, a sintaxe exigirá o nome principal do servidor, que é o nome do computador de destino em vez do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="bdbbe-110">Você pode usar o parâmetro Authority somente com conexões com servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="bdbbe-111">A tentativa de conexão falhará se você tentar definir níveis de autorização como parte de um moniker ou com uma chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) para uma conexão local.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="bdbbe-112">Execute o procedimento a seguir para especificar o serviço de autenticação que você deseja usar no parâmetro *strAuthority* do método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou a conexão de cadeia de caracteres do [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="bdbbe-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="bdbbe-113">**Para especificar a autenticação NTLM ou Kerberos com a API de script para WMI**</span><span class="sxs-lookup"><span data-stu-id="bdbbe-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="bdbbe-114">Se o parâmetro *strAuthority* começar com a cadeia de caracteres "Kerberos:", o WMI assumirá que a cadeia de caracteres se refere a um nome de entidade Kerberos e a autenticação Kerberos será usada.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="bdbbe-115">Se o parâmetro *strAuthority* começar com a cadeia de caracteres "NTLMDOMAIN:", o WMI usará a autenticação NTLM em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="bdbbe-116">Como alternativa, você pode usar a parte da autoridade de um moniker para especificar o tipo de autenticação usado para se conectar ao WMI.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="bdbbe-117">Para usar a autenticação Kerberos ao usar um moniker, inclua a cadeia de caracteres "Authority = Kerberos:" seguida pelo nome principal.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="bdbbe-118">Para usar a autenticação NTLM, inclua a cadeia de caracteres "Authority = NTLMDOMAIN:" seguida pelo nome de domínio NTLM.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="bdbbe-119">O exemplo a seguir mostra um moniker que solicita a autenticação Kerberos usando o "servidor mydomain \\ " principal.</span><span class="sxs-lookup"><span data-stu-id="bdbbe-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="bdbbe-120">Por outro lado, o exemplo a seguir mostra um moniker que solicita a autenticação NTLM usando o domínio "mydomain".</span><span class="sxs-lookup"><span data-stu-id="bdbbe-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



