---
description: A propriedade AuthenticationLevel é um inteiro que define o nível de autenticação COM que é atribuído a esse objeto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity. AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296591"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="3df52-103">Propriedade SWbemSecurity. AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="3df52-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="3df52-104">A propriedade **AuthenticationLevel** é um inteiro que define o nível de autenticação com que é atribuído a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="3df52-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="3df52-105">Essa configuração determina como você protege as informações enviadas do WMI.</span><span class="sxs-lookup"><span data-stu-id="3df52-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="3df52-106">Para obter mais informações sobre níveis de autenticação, consulte [definindo a \_ segurança do \_ processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="3df52-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="3df52-107">Em geral, não é necessário definir o nível de autenticação ao fazer chamadas de API do WMI.</span><span class="sxs-lookup"><span data-stu-id="3df52-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="3df52-108">Se você não definir essa propriedade, o nível de autenticação COM padrão para seu sistema será usado.</span><span class="sxs-lookup"><span data-stu-id="3df52-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="3df52-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3df52-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3df52-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3df52-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df52-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3df52-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="3df52-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3df52-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3df52-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3df52-113">Remarks</span></span>

<span data-ttu-id="3df52-114">A configuração authenticationLevel permite solicitar o nível de autenticação DCOM e privacidade a ser usada em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="3df52-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="3df52-115">O intervalo de configurações não é autenticado para autenticação criptografada por pacote.</span><span class="sxs-lookup"><span data-stu-id="3df52-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="3df52-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3df52-116">Value</span></span>        | <span data-ttu-id="3df52-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3df52-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df52-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3df52-118">None</span></span>         | <span data-ttu-id="3df52-119">Não usa nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="3df52-119">Does not use any authentication.</span></span> <span data-ttu-id="3df52-120">Todas as configurações de segurança são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="3df52-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="3df52-121">Padrão</span><span class="sxs-lookup"><span data-stu-id="3df52-121">Default</span></span>      | <span data-ttu-id="3df52-122">Usa uma negociação de segurança padrão para selecionar um nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3df52-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="3df52-123">Essa é a configuração recomendada porque o cliente envolvido na transação será negociado para o nível de autenticação especificado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="3df52-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="3df52-124">O DCOM não selecionará o valor None durante uma sessão de negociação.</span><span class="sxs-lookup"><span data-stu-id="3df52-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="3df52-125">Conectar</span><span class="sxs-lookup"><span data-stu-id="3df52-125">Connect</span></span>      | <span data-ttu-id="3df52-126">Autentica as credenciais do cliente somente quando o cliente tenta se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="3df52-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="3df52-127">Depois que uma conexão é estabelecida, nenhuma verificação de autenticação adicional ocorre.</span><span class="sxs-lookup"><span data-stu-id="3df52-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="3df52-128">Chamar</span><span class="sxs-lookup"><span data-stu-id="3df52-128">Call</span></span>         | <span data-ttu-id="3df52-129">Autentica as credenciais do cliente somente no início de cada chamada, quando o servidor recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3df52-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="3df52-130">Os cabeçalhos de pacote são assinados, mas os pacotes de dados trocados entre o cliente e o servidor não são assinados nem criptografados.</span><span class="sxs-lookup"><span data-stu-id="3df52-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="3df52-131">PCT</span><span class="sxs-lookup"><span data-stu-id="3df52-131">Pkt</span></span>          | <span data-ttu-id="3df52-132">Autentica que todos os pacotes de dados são recebidos do cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="3df52-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="3df52-133">Semelhante a chamada; os cabeçalhos de pacote são assinados, mas não criptografados.</span><span class="sxs-lookup"><span data-stu-id="3df52-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="3df52-134">Os próprios pacotes não são assinados nem criptografados.</span><span class="sxs-lookup"><span data-stu-id="3df52-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="3df52-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="3df52-135">PktIntegrity</span></span> | <span data-ttu-id="3df52-136">Autentica e verifica se nenhum dos pacotes de dados transferidos entre o cliente e o servidor foi modificado.</span><span class="sxs-lookup"><span data-stu-id="3df52-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="3df52-137">Cada pacote de dados é assinado, garantindo que os pacotes não tenham sido modificados durante o trânsito.</span><span class="sxs-lookup"><span data-stu-id="3df52-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="3df52-138">Nenhum dos pacotes de dados está criptografado.</span><span class="sxs-lookup"><span data-stu-id="3df52-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="3df52-139">PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="3df52-139">PktPrivacy</span></span>   | <span data-ttu-id="3df52-140">Autentica todos os níveis de representação anteriores e assina e criptografa cada pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="3df52-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="3df52-141">Isso garante que toda a comunicação entre o cliente e o servidor seja confidencial.</span><span class="sxs-lookup"><span data-stu-id="3df52-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="3df52-142">Você pode definir o nível de autenticação dos objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) definindo a propriedade **AuthenticationLevel** para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="3df52-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="3df52-143">O exemplo a seguir mostra como definir o nível de autenticação para um objeto **SwbemObject** .</span><span class="sxs-lookup"><span data-stu-id="3df52-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="3df52-144">Você também pode especificar níveis de autenticação como parte de um moniker.</span><span class="sxs-lookup"><span data-stu-id="3df52-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="3df52-145">O exemplo a seguir define o nível de autenticação e o nível de representação e recupera uma instância do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="3df52-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="3df52-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df52-146">Requirements</span></span>



| <span data-ttu-id="3df52-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df52-147">Requirement</span></span> | <span data-ttu-id="3df52-148">Valor</span><span class="sxs-lookup"><span data-stu-id="3df52-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df52-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df52-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3df52-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3df52-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3df52-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df52-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3df52-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3df52-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3df52-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3df52-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="3df52-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3df52-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3df52-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3df52-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df52-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df52-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3df52-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="3df52-157">CLSID</span></span><br/>                    | <span data-ttu-id="3df52-158">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="3df52-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="3df52-159">IID</span><span class="sxs-lookup"><span data-stu-id="3df52-159">IID</span></span><br/>                      | <span data-ttu-id="3df52-160">ISWbemSecurity de IID \_</span><span class="sxs-lookup"><span data-stu-id="3df52-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3df52-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="3df52-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df52-162">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="3df52-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="3df52-163">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="3df52-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="3df52-164">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="3df52-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

