---
title: Valores do registro do método de par EAP
description: Saiba mais sobre os valores de registro específicos que são necessários para métodos de par EAP. Consulte uma lista de valores do registro e exiba recursos adicionais disponíveis.
ms.assetid: 16bdd6bf-9eab-40a8-a2d3-8942d2f5f37a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796260a25f824ffe52ada7cdfadfb7a25f05d491
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294512"
---
# <a name="eap-peer-method-registry-values"></a><span data-ttu-id="462c2-104">Valores do registro do método de par EAP</span><span class="sxs-lookup"><span data-stu-id="462c2-104">EAP Peer Method Registry Values</span></span>

<span data-ttu-id="462c2-105">Valores de registro específicos são necessários para métodos de par EAP.</span><span class="sxs-lookup"><span data-stu-id="462c2-105">Specific registry values are required for EAP peer methods.</span></span>

## <a name="eap-peer-method-dll-paths"></a><span data-ttu-id="462c2-106">Caminhos de DLL do método EAP peer</span><span class="sxs-lookup"><span data-stu-id="462c2-106">EAP Peer Method DLL Paths</span></span>

<span data-ttu-id="462c2-107">O caminho a seguir especifica o local do registro para DLLs do método EAP de mesmo nível regulares.</span><span class="sxs-lookup"><span data-stu-id="462c2-107">The following path specifies the registry location for regular EAP peer method DLLs.</span></span>

<span data-ttu-id="462c2-108">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="462c2-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="462c2-109">Por exemplo, um caminho de registro de instalação do método EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e um **EapTypeId** de "40", aparece da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="462c2-109">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="462c2-110">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="462c2-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="462c2-111">O caminho a seguir especifica o local do registro para as DLLs do método EAP estendido.</span><span class="sxs-lookup"><span data-stu-id="462c2-111">The following path specifies the registry location for extended EAP method DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="462c2-112">As DLLs de método EAP estendidas têm suporte no Windows Vista com Service Pack 1 (SP1) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="462c2-112">Extended EAP method DLLs are supported in Windows Vista with Service Pack 1 (SP1) or later.</span></span>

 

<span data-ttu-id="462c2-113">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="462c2-113">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="462c2-114">Por exemplo, um caminho de registro de instalação do método EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **vendorid** de "311" e um **EapTypeId** de "40", aparece da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="462c2-114">For example, an EAP method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="462c2-115">**HKLM \\ System \\ ccs \\ Services \\ Eaphost \\ métodos \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="462c2-115">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="462c2-116">Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6,2 do [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="462c2-116">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="462c2-117">Valores do registro</span><span class="sxs-lookup"><span data-stu-id="462c2-117">Registry Values</span></span>

<span data-ttu-id="462c2-118">Os seguintes valores de registro do método de par do EAPHost são necessários.</span><span class="sxs-lookup"><span data-stu-id="462c2-118">The following EAPHost peer method registry values are required.</span></span>

-   [<span data-ttu-id="462c2-119">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="462c2-119">PeerDllPath</span></span>](#peerdllpath)
-   [<span data-ttu-id="462c2-120">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="462c2-120">PeerFriendlyName</span></span>](#peerfriendlyname)
-   [<span data-ttu-id="462c2-121">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-121">PeerInvokePasswordDialog</span></span>](#peerinvokepassworddialog)
-   [<span data-ttu-id="462c2-122">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-122">PeerInvokeUsernameDialog</span></span>](#peerinvokeusernamedialog)

<span data-ttu-id="462c2-123">Os seguintes valores de registro do método peer do AP são recomendados.</span><span class="sxs-lookup"><span data-stu-id="462c2-123">The following AP peer method registry values are recommended.</span></span>

-   [<span data-ttu-id="462c2-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="462c2-124">Properties</span></span>](#properties)

<span data-ttu-id="462c2-125">Os seguintes valores de registro do método peer do AP são opcionais.</span><span class="sxs-lookup"><span data-stu-id="462c2-125">The following AP peer method registry values are optional.</span></span>

-   [<span data-ttu-id="462c2-126">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-126">PeerConfigUIPath</span></span>](#peerconfiguipath)
-   [<span data-ttu-id="462c2-127">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="462c2-127">PeerIdentityPath</span></span>](#peeridentitypath)
-   [<span data-ttu-id="462c2-128">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-128">PeerInteractiveUIPath</span></span>](#peerinteractiveuipath)
-   [<span data-ttu-id="462c2-129">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="462c2-129">PeerRequireConfigUI</span></span>](#peerrequireconfigui)

### <a name="peerconfiguipath"></a><span data-ttu-id="462c2-130">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-130">PeerConfigUIPath</span></span>



| <span data-ttu-id="462c2-131">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-131">Constant Value</span></span> | <span data-ttu-id="462c2-132">PeerConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-132">PeerConfigUIPath</span></span>                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-133">Type</span></span>           | <span data-ttu-id="462c2-134">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="462c2-134">REG\_EXPAND\_SZ</span></span>                                                                                                                                        |
| <span data-ttu-id="462c2-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-135">Description</span></span>    | <span data-ttu-id="462c2-136">O caminho para a DLL que contém a implementação da caixa de diálogo de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="462c2-136">The path to the DLL that contains the implementation of the user configuration dialog.</span></span> <span data-ttu-id="462c2-137">Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="462c2-137">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerdllpath"></a><span data-ttu-id="462c2-138">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="462c2-138">PeerDllPath</span></span>



| <span data-ttu-id="462c2-139">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-139">Constant Value</span></span> | <span data-ttu-id="462c2-140">PeerDllPath</span><span class="sxs-lookup"><span data-stu-id="462c2-140">PeerDllPath</span></span>                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-141">Type</span></span>           | <span data-ttu-id="462c2-142">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="462c2-142">REG\_EXPAND\_SZ</span></span>                                                                                 |
| <span data-ttu-id="462c2-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-143">Description</span></span>    | <span data-ttu-id="462c2-144">O caminho para a DLL do método EAP.</span><span class="sxs-lookup"><span data-stu-id="462c2-144">The path to the EAP method DLL.</span></span> <span data-ttu-id="462c2-145">Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="462c2-145">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerfriendlyname"></a><span data-ttu-id="462c2-146">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="462c2-146">PeerFriendlyName</span></span>



| <span data-ttu-id="462c2-147">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-147">Constant Value</span></span> | <span data-ttu-id="462c2-148">PeerFriendlyName</span><span class="sxs-lookup"><span data-stu-id="462c2-148">PeerFriendlyName</span></span>                                                     |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="462c2-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-149">Type</span></span>           | <span data-ttu-id="462c2-150">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="462c2-150">REG\_SZ</span></span>                                                              |
| <span data-ttu-id="462c2-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-151">Description</span></span>    | <span data-ttu-id="462c2-152">Cadeia de caracteres que contém o nome amigável (exibição) para o método EAP.</span><span class="sxs-lookup"><span data-stu-id="462c2-152">String that contains the friendly (display) name for the EAP method.</span></span> |



 

### <a name="peeridentitypath"></a><span data-ttu-id="462c2-153">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="462c2-153">PeerIdentityPath</span></span>



| <span data-ttu-id="462c2-154">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-154">Constant Value</span></span> | <span data-ttu-id="462c2-155">PeerIdentityPath</span><span class="sxs-lookup"><span data-stu-id="462c2-155">PeerIdentityPath</span></span>                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-156">Type</span></span>           | <span data-ttu-id="462c2-157">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="462c2-157">REG\_EXPAND\_SZ</span></span>                                                                                                                                      |
| <span data-ttu-id="462c2-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-158">Description</span></span>    | <span data-ttu-id="462c2-159">O caminho para a DLL que contém a implementação das funções de identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="462c2-159">The path to the DLL that contains the implementation of the user identity functions.</span></span> <span data-ttu-id="462c2-160">Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="462c2-160">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinteractiveuipath"></a><span data-ttu-id="462c2-161">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-161">PeerInteractiveUIPath</span></span>



| <span data-ttu-id="462c2-162">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-162">Constant Value</span></span> | <span data-ttu-id="462c2-163">PeerInteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="462c2-163">PeerInteractiveUIPath</span></span>                                                                                                                                                                                                      |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-164">Type</span></span>           | <span data-ttu-id="462c2-165">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="462c2-165">REG\_EXPAND\_SZ</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="462c2-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-166">Description</span></span>    | <span data-ttu-id="462c2-167">O caminho para a DLL que contém a implementação da interface do usuário interativa usada para obter informações do usuário durante a execução do método EAP.</span><span class="sxs-lookup"><span data-stu-id="462c2-167">The path to the DLL that contains the implementation of the interactive user interface used to obtain user information during execution of the EAP method.</span></span> <span data-ttu-id="462c2-168">Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="462c2-168">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

### <a name="peerinvokepassworddialog"></a><span data-ttu-id="462c2-169">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-169">PeerInvokePasswordDialog</span></span>



| <span data-ttu-id="462c2-170">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-170">Constant Value</span></span> | <span data-ttu-id="462c2-171">PeerInvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-171">PeerInvokePasswordDialog</span></span>                                                                                                                                                                                                                         |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-172">Type</span></span>           | <span data-ttu-id="462c2-173">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="462c2-173">REG\_DWORD</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="462c2-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-174">Description</span></span>    | <span data-ttu-id="462c2-175">1-para obter credenciais usando a caixa de diálogo de senha e domínio do EAPHost genérico.</span><span class="sxs-lookup"><span data-stu-id="462c2-175">1- to get credentials using the generic EAPHost password and domain dialog box.</span></span> <span data-ttu-id="462c2-176">0-para usar uma caixa de diálogo personalizada.</span><span class="sxs-lookup"><span data-stu-id="462c2-176">0 - to use a custom dialog box.</span></span> <span data-ttu-id="462c2-177">Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo método [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="462c2-177">If the generic dialog box is used, credentials are set by the [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span> |



 

### <a name="peerinvokeusernamedialog"></a><span data-ttu-id="462c2-178">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-178">PeerInvokeUsernameDialog</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="462c2-179">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-179">Constant Value</span></span></th>
<th><span data-ttu-id="462c2-180">PeerInvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="462c2-180">PeerInvokeUsernameDialog</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="462c2-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-181">Type</span></span></td>
<td><span data-ttu-id="462c2-182">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="462c2-182">REG_DWORD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="462c2-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-183">Description</span></span></td>
<td><ul>
<li><span data-ttu-id="462c2-184">1-para obter credenciais usando a caixa de diálogo nome de usuário do EAPHost genérico.</span><span class="sxs-lookup"><span data-stu-id="462c2-184">1 - to get credentials using the generic EAPHost user name dialog box.</span></span></li>
<li><span data-ttu-id="462c2-185">0-para usar uma caixa de diálogo personalizada.</span><span class="sxs-lookup"><span data-stu-id="462c2-185">0- to use a custom dialog box.</span></span></li>
</ul>
<span data-ttu-id="462c2-186">Se a caixa de diálogo genérica for usada, as credenciais serão definidas pelo método [<strong>EapPeerSetCredentials</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetcredentials).</span><span class="sxs-lookup"><span data-stu-id="462c2-186">If the generic dialog box is used, credentials are set by the [<strong>EapPeerSetCredentials</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials) method.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="peerrequireconfigui"></a><span data-ttu-id="462c2-187">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="462c2-187">PeerRequireConfigUI</span></span>



| <span data-ttu-id="462c2-188">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-188">Constant Value</span></span> | <span data-ttu-id="462c2-189">PeerRequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="462c2-189">PeerRequireConfigUI</span></span>                                                                        |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-190">Type</span></span>           | <span data-ttu-id="462c2-191">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="462c2-191">REG\_DWORD</span></span>                                                                                 |
| <span data-ttu-id="462c2-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-192">Description</span></span>    | <span data-ttu-id="462c2-193">0 se uma caixa de diálogo de interface de usuário de configuração for implementada para esse método; 1 se não for.</span><span class="sxs-lookup"><span data-stu-id="462c2-193">0 if a configuration user interface dialog is implemented for this method; 1 if it is not.</span></span> |



 

### <a name="properties"></a><span data-ttu-id="462c2-194">Propriedades</span><span class="sxs-lookup"><span data-stu-id="462c2-194">Properties</span></span>



| <span data-ttu-id="462c2-195">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="462c2-195">Constant Value</span></span> | <span data-ttu-id="462c2-196">Propriedades</span><span class="sxs-lookup"><span data-stu-id="462c2-196">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462c2-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="462c2-197">Type</span></span>           | <span data-ttu-id="462c2-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="462c2-198">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="462c2-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="462c2-199">Description</span></span>    | <span data-ttu-id="462c2-200">Os bits no DWORD são definidos para indicar suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="462c2-200">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="462c2-201">Para obter uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="462c2-201">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="462c2-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="462c2-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="462c2-203">Chaves do registro do método de autenticador EAP</span><span class="sxs-lookup"><span data-stu-id="462c2-203">EAP Authenticator Method Registry Keys</span></span>](eap-authenticator-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="462c2-204">Configuração do registro para tipos de EAP expandidos</span><span class="sxs-lookup"><span data-stu-id="462c2-204">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="462c2-205">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="462c2-205">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="462c2-206">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="462c2-206">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 