---
title: Constantes de autenticação (WSManDisp. h)
description: Especifique o método de autenticação e como lidar com servidores de certificado para transporte HTTPS de solicitações.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499706"
---
# <a name="authentication-constants"></a><span data-ttu-id="0b504-103">Constantes de autenticação</span><span class="sxs-lookup"><span data-stu-id="0b504-103">Authentication Constants</span></span>

<span data-ttu-id="0b504-104">As constantes de autenticação são constantes na enumeração **\_ \_ WSManSessionFlags** que especificam o método de autenticação e como lidar com servidores de certificado para transporte HTTPS de solicitações.</span><span class="sxs-lookup"><span data-stu-id="0b504-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="0b504-105">Uma ou mais das constantes listadas na lista a seguir são necessárias no parâmetro *flags* em chamadas para [**WSMan. CreateSession**](wsman-createsession.md) ou em chamadas [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectam a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="0b504-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="0b504-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="0b504-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="0b504-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-108">Use o nome de usuário e a senha como as credenciais.</span><span class="sxs-lookup"><span data-stu-id="0b504-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="0b504-109">Defina esse sinalizador ao criar um objeto [**ConnectionOptions**](connectionoptions.md) e fornecer o [**nome de usuário**](connectionoptions-username.md) e a [**senha**](connectionoptions-password.md).</span><span class="sxs-lookup"><span data-stu-id="0b504-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="0b504-110">As credenciais podem ser uma conta de domínio ou uma conta no computador local.</span><span class="sxs-lookup"><span data-stu-id="0b504-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="0b504-111">Por padrão, a conta deve ser um membro do grupo local de administradores no computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="0b504-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="0b504-112">No entanto, o serviço WinRM pode ser configurado para permitir outros usuários.</span><span class="sxs-lookup"><span data-stu-id="0b504-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="0b504-113">Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="0b504-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="0b504-114">Você pode definir esse sinalizador ao especificar credenciais para autenticação de negociação (também conhecida como [*autenticação integrada do Windows*](windows-remote-management-glossary.md)) ou para [*autenticação básica*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b504-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="0b504-115">O método de script associado é [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)e o método C++ é [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span><span class="sxs-lookup"><span data-stu-id="0b504-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="0b504-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="0b504-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-118">Ao se conectar via HTTPS, o cliente não valida se o certificado do servidor está assinado por uma autoridade de certificação (CA) confiável.</span><span class="sxs-lookup"><span data-stu-id="0b504-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="0b504-119">Use esse valor somente quando o computador remoto for confiável por outros meios, por exemplo, se o computador remoto fizer parte de uma rede que esteja fisicamente segura e isolada ou o computador remoto estiver listado como um host confiável na configuração do WinRM.</span><span class="sxs-lookup"><span data-stu-id="0b504-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="0b504-120">O método de script associado é [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)e o método C++ é [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="0b504-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="0b504-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="0b504-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-123">Ao se conectar via HTTPS, o cliente não validará que o CN (nome comum) no certificado do servidor corresponde ao nome do computador na cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="0b504-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="0b504-124">Use somente quando o computador remoto for confiável por outros meios, por exemplo, se o computador remoto fizer parte de uma rede fisicamente segura e isolada ou se o computador remoto estiver listado como um host confiável na configuração do WinRM.</span><span class="sxs-lookup"><span data-stu-id="0b504-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="0b504-125">O método de script associado é [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)e o método C++ é [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span><span class="sxs-lookup"><span data-stu-id="0b504-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="0b504-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-127">32768 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="0b504-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-128">Não use nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="0b504-128">Use no authentication.</span></span> <span data-ttu-id="0b504-129">Especifique essa constante ao testar uma conexão com um computador remoto para determinar se um serviço que implementa o protocolo de WS-Management está configurado para escutar solicitações de dados.</span><span class="sxs-lookup"><span data-stu-id="0b504-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="0b504-130">**WSManFlagUseNoAuthentication** não pode ser combinado com nenhuma outra constante de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="0b504-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="0b504-131">O método de script associado é [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)e o método C++ é [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="0b504-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="0b504-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="0b504-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-134">Use a autenticação Digest.</span><span class="sxs-lookup"><span data-stu-id="0b504-134">Use Digest authentication.</span></span> <span data-ttu-id="0b504-135">Apenas o computador cliente pode iniciar uma solicitação de autenticação Digest.</span><span class="sxs-lookup"><span data-stu-id="0b504-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="0b504-136">O cliente envia uma solicitação ao servidor para autenticar e receber uma cadeia de caracteres de token do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b504-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="0b504-137">Em seguida, o cliente envia a solicitação de recurso, incluindo o nome de usuário e um hash criptográfico da senha combinada com a cadeia de caracteres do token.</span><span class="sxs-lookup"><span data-stu-id="0b504-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="0b504-138">A autenticação Digest tem suporte para HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0b504-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="0b504-139">Os aplicativos e scripts do cliente WinRM podem especificar a autenticação Digest, mas não o serviço.</span><span class="sxs-lookup"><span data-stu-id="0b504-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="0b504-140">O método de script associado é [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)e o método C++ é [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="0b504-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="0b504-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="0b504-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-143">Use a autenticação de negociação.</span><span class="sxs-lookup"><span data-stu-id="0b504-143">Use Negotiate authentication.</span></span> <span data-ttu-id="0b504-144">O cliente envia uma solicitação ao servidor para autenticar.</span><span class="sxs-lookup"><span data-stu-id="0b504-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="0b504-145">O servidor determina se o Kerberos ou NTLM deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="0b504-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="0b504-146">O Kerberos está selecionado para autenticar uma conta de domínio e o NTLM está selecionado para contas de computador local.</span><span class="sxs-lookup"><span data-stu-id="0b504-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="0b504-147">O nome de usuário deve ser especificado no formato domínio \\ nome de usuário para um domínio user ou ServerName \\ username para um usuário local em um computador servidor.</span><span class="sxs-lookup"><span data-stu-id="0b504-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="0b504-148">O [UAC (controle de conta de usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afeta o acesso ao serviço WinRM.</span><span class="sxs-lookup"><span data-stu-id="0b504-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="0b504-149">Quando a autenticação de negociação é usada em um grupo de trabalho ou domínio, somente a conta de administrador interno pode acessar o serviço.</span><span class="sxs-lookup"><span data-stu-id="0b504-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="0b504-150">Para permitir que todas as contas no grupo administradores acessem o serviço, defina a seguinte chave do registro como 1: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="0b504-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="0b504-151">O método de script associado é [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)e o método C++ é [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="0b504-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="0b504-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="0b504-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-154">Use a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="0b504-154">Use Basic authentication.</span></span> <span data-ttu-id="0b504-155">O cliente apresenta credenciais na forma de um nome de usuário e senha, transmitidos diretamente na mensagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="0b504-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="0b504-156">Você pode especificar apenas as credenciais que identificam uma conta de administrador local no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="0b504-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="0b504-157">O método de script associado é [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)e o método C++ é [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span><span class="sxs-lookup"><span data-stu-id="0b504-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="0b504-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="0b504-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-160">Usar a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0b504-160">Use Kerberos authentication.</span></span> <span data-ttu-id="0b504-161">O cliente e o servidor se autenticam mutuamente usando tíquetes Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0b504-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="0b504-162">O método de script associado é [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)e o método C++ é [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="0b504-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="0b504-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-164">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="0b504-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-165">Não use criptografia.</span><span class="sxs-lookup"><span data-stu-id="0b504-165">Use no encryption.</span></span> <span data-ttu-id="0b504-166">O tráfego não criptografado não é permitido por padrão e deve ser habilitado no cliente e no servidor.</span><span class="sxs-lookup"><span data-stu-id="0b504-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="0b504-167">O método de script associado é [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)e o método C++ é [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="0b504-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="0b504-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-169">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="0b504-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-170">Use a autenticação baseada em certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="0b504-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="0b504-171">O método de script associado é [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)e o método C++ é [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="0b504-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span><span class="sxs-lookup"><span data-stu-id="0b504-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="0b504-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="0b504-174">Use a autenticação do Credential Security Support Provider (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="0b504-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="0b504-175">O método de script associado é [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)e o método C++ é [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="0b504-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="0b504-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="0b504-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="0b504-178">Não verificar revogação de certificado durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="0b504-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span><span class="sxs-lookup"><span data-stu-id="0b504-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="0b504-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="0b504-181">Permitir credenciais implícitas.</span><span class="sxs-lookup"><span data-stu-id="0b504-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b504-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span><span class="sxs-lookup"><span data-stu-id="0b504-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b504-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="0b504-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="0b504-184">Usar camada de soquete seguro, habilita HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0b504-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b504-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b504-185">Requirements</span></span>



| <span data-ttu-id="0b504-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b504-186">Requirement</span></span> | <span data-ttu-id="0b504-187">Valor</span><span class="sxs-lookup"><span data-stu-id="0b504-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b504-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b504-188">Minimum supported client</span></span><br/> | <span data-ttu-id="0b504-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b504-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0b504-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b504-190">Minimum supported server</span></span><br/> | <span data-ttu-id="0b504-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b504-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b504-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b504-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b504-193"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b504-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b504-194">INSERI</span><span class="sxs-lookup"><span data-stu-id="0b504-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b504-195"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b504-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b504-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b504-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b504-197">Constantes de sessão</span><span class="sxs-lookup"><span data-stu-id="0b504-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





