---
title: Método WSMan. CreateSession (WSManDisp. h)
description: Cria um objeto de sessão que pode ser usado para operações de rede subsequentes.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Método CreateSession Gerenciamento Remoto do Windows
- Método CreateSession Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499496"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="e4a6a-106">Método WSMan. CreateSession</span><span class="sxs-lookup"><span data-stu-id="e4a6a-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="e4a6a-107">Cria um objeto de [**sessão**](session.md) que pode ser usado para operações de rede subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a6a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4a6a-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e4a6a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4a6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a6a-110">*conexão* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e4a6a-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a6a-111">O protocolo e o serviço aos quais se conectar, incluindo o IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="e4a6a-112">O formato das informações de conexão é o seguinte: <sufixo de endereço de *transporte* ><  >< >.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="e4a6a-113">Para obter exemplos, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-113">For examples, see Remarks.</span></span> <span data-ttu-id="e4a6a-114">Se nenhuma informação de conexão for fornecida, o computador local será usado.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="e4a6a-115">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e4a6a-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a6a-116">Os sinalizadores de sessão que especificam o método de autenticação, como [*autenticação de negociação*](windows-remote-management-glossary.md) ou [*autenticação Digest*](windows-remote-management-glossary.md), para conexão a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="e4a6a-117">Esses sinalizadores também especificam outras informações de conexão de sessão, como codificação ou criptografia.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="e4a6a-118">Esse parâmetro deve conter um ou mais dos sinalizadores em **\_ \_ WSManSessionFlags** para uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="e4a6a-119">Para obter mais informações, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6a-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="e4a6a-120">Nenhuma configuração de sinalizador é necessária para uma conexão com o WinRM no computador local.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="e4a6a-121">O padrão é **WSManFlagUseNegotiate**.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="e4a6a-122">Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md) e o parâmetro *ConnectionOptions* .</span><span class="sxs-lookup"><span data-stu-id="e4a6a-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e4a6a-123">*ConnectionOptions* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e4a6a-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a6a-124">Um ponteiro para um objeto [**ConnectionOptions**](connectionoptions.md) que contém um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="e4a6a-125">O padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a6a-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4a6a-126">Return value</span></span>

<span data-ttu-id="e4a6a-127">Um objeto de [**sessão**](session.md) que pode ser usado para executar operações WinRM locais ou remotas.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4a6a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4a6a-128">Remarks</span></span>

<span data-ttu-id="e4a6a-129">O método **CreateSession** Inicializa o objeto de [**sessão**](session.md) coletando parâmetros, como sinalizadores, credenciais e uma cadeia de conexão para o parâmetro de *conexão* .</span><span class="sxs-lookup"><span data-stu-id="e4a6a-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="e4a6a-130">**CreateSession** não se conecta de fato ao computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="e4a6a-131">Se a conexão não puder ser estabelecida, ocorrerá uma falha na primeira operação de **sessão** , como [**obter**](session-get.md) ou [**enumerar**](session-enumerate.md), após a chamada para **CreateSession**.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="e4a6a-132">Esse comportamento é diferente de uma conexão [*WMI*](windows-remote-management-glossary.md) com um [*namespace*](windows-remote-management-glossary.md) em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="e4a6a-133">Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6a-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="e4a6a-134">O exemplo de código VBScript a seguir é usado para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="e4a6a-135">Os exemplos a seguir mostram os diferentes formatos usados para especificar informações de conexão no parâmetro de *conexão* (ao criar uma sessão HTTPS, o campo de> de *endereço* <deve corresponder ao nome do certificado do computador do servidor; caso contrário, ocorre uma falha):</span><span class="sxs-lookup"><span data-stu-id="e4a6a-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="e4a6a-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="e4a6a-136">"https://service"</span></span>

    <span data-ttu-id="e4a6a-137">Usa HTTPS para se conectar ao local do serviço Web padrão.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="e4a6a-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="e4a6a-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="e4a6a-139">Usa HTTPS para se conectar ao local específico do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="e4a6a-140">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="e4a6a-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="e4a6a-141">Usa HTTPS e IPv6 com a porta padrão.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="e4a6a-142">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/WSMan"</span><span class="sxs-lookup"><span data-stu-id="e4a6a-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="e4a6a-143">Usa HTTPS e IPv6 com a porta fornecida.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="e4a6a-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4a6a-144">Examples</span></span>

<span data-ttu-id="e4a6a-145">O exemplo de código VBScript a seguir cria uma sessão no computador local.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="e4a6a-146">O exemplo de código VBScript a seguir cria uma sessão em um computador remoto que é identificada por um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="e4a6a-147">O script fornece um nome de usuário e uma senha para uma conta.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="e4a6a-148">Os sinalizadores **WSManFlagCredUserNamePassword** e **WSManFlagUseBasic** são combinados para indicar que a conta é uma conta local no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="e4a6a-149">Se a criação da sessão falhar, o script será encerrado.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="e4a6a-150">O script usa os métodos que retornam a constante, como [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6a-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="e4a6a-151">Para executar esse script, lembre-se de que você deve definir as definições de configuração padrão para cliente e servidor para permitir tráfego não criptografado e autenticação básica (**AllowUnencrypted** definido como **true** e Basic definido como **true**).</span><span class="sxs-lookup"><span data-stu-id="e4a6a-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="e4a6a-152">Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="e4a6a-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="e4a6a-153">No exemplo de código VBScript a seguir, a conta é uma conta de domínio e a autenticação de negociação é usada.</span><span class="sxs-lookup"><span data-stu-id="e4a6a-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="e4a6a-154">Com a autenticação de negociação, você deve especificar o nome de usuário como `computername\username` ou `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="e4a6a-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="e4a6a-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4a6a-155">Requirements</span></span>



| <span data-ttu-id="e4a6a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a6a-156">Requirement</span></span> | <span data-ttu-id="e4a6a-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e4a6a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a6a-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a6a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a6a-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4a6a-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e4a6a-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a6a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a6a-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4a6a-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e4a6a-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4a6a-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a6a-163"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a6a-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4a6a-164">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4a6a-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4a6a-165"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4a6a-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4a6a-166">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4a6a-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4a6a-167"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e4a6a-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e4a6a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="e4a6a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4a6a-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4a6a-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4a6a-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4a6a-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a6a-171">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="e4a6a-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="e4a6a-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e4a6a-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="e4a6a-173">**Session**</span><span class="sxs-lookup"><span data-stu-id="e4a6a-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="e4a6a-174">Autenticação para conexões remotas</span><span class="sxs-lookup"><span data-stu-id="e4a6a-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="e4a6a-175">Instalação e configuração para Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="e4a6a-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





