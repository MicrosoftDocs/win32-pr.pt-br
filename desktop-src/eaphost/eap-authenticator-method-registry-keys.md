---
title: Valores de registro do método de autenticador EAP
description: Saiba mais sobre os valores de registro do método de autenticador EAP. Esses valores de registro específicos são necessários para métodos de autenticador EAP.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917690"
---
# <a name="eap-authenticator-method-registry-values"></a><span data-ttu-id="da819-104">Valores de registro do método de autenticador EAP</span><span class="sxs-lookup"><span data-stu-id="da819-104">EAP Authenticator Method Registry Values</span></span>

<span data-ttu-id="da819-105">Valores de registro específicos são necessários para métodos de autenticador EAP.</span><span class="sxs-lookup"><span data-stu-id="da819-105">Specific registry values are required for EAP authenticator methods.</span></span>

## <a name="eap-authenticator-method-dll-paths"></a><span data-ttu-id="da819-106">Caminhos de DLL do método de autenticador EAP</span><span class="sxs-lookup"><span data-stu-id="da819-106">EAP Authenticator Method DLL Paths</span></span>

<span data-ttu-id="da819-107">O caminho a seguir especifica o local do registro para DLLs de método de autenticador EAP regulares.</span><span class="sxs-lookup"><span data-stu-id="da819-107">The following path specifies the registry location for regular EAP authenticator method DLLs.</span></span>

<span data-ttu-id="da819-108">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ \* &lt; EapTypeId&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="da819-108">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\*&lt;EapTypeId&gt;**\*</span></span>

<span data-ttu-id="da819-109">Por exemplo, um caminho de registro de instalação do método de autenticador EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor) e um **EapTypeId** de "40", aparece da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="da819-109">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author) and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="da819-110">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="da819-110">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\40**</span></span>

<span data-ttu-id="da819-111">O caminho a seguir especifica o local do registro para as DLLs do método de autenticador EAP estendido.</span><span class="sxs-lookup"><span data-stu-id="da819-111">The following path specifies the registry location for extended EAP authenticator method DLLs.</span></span>

<span data-ttu-id="da819-112">**HKLM \\ System \\ ccs \\ Services \\ EAPHost \\ métodos \\ *&lt; AuthorId &gt;* \\ 254 \\ *&lt; VendorID &gt;* VendorID \\ \* &lt;&gt;**\*</span><span class="sxs-lookup"><span data-stu-id="da819-112">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\*&lt;AuthorId&gt;*\\254\\*&lt;VendorId&gt;*\\*&lt;VendorType&gt;**\*</span></span>

<span data-ttu-id="da819-113">Por exemplo, um caminho de registro de instalação do método de autenticador EAP, dado um **AuthorId** de "311" (indicando que "Microsoft" é o autor), um **vendorid** de "311" e um **EapTypeId** de "40", aparece da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="da819-113">For example, an EAP authenticator method installation registration path given an **AuthorId** of "311" (indicating that "Microsoft" is the author), a **VendorId** of "311", and a **EapTypeId** of "40", appears as follows.</span></span>

<span data-ttu-id="da819-114">**HKLM \\ System \\ ccs \\ Services \\ Eaphost \\ métodos \\ 311 \\ 254 \\ 311 \\ 40**</span><span class="sxs-lookup"><span data-stu-id="da819-114">**HKLM\\System\\CCS\\Services\\Eaphost\\Methods\\311\\254\\311\\40**</span></span>

> [!Note]  
> <span data-ttu-id="da819-115">Para obter mais informações sobre a alocação de tipos de método EAP, consulte a seção 6,2 do [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span><span class="sxs-lookup"><span data-stu-id="da819-115">For more information on the allocation of EAP method types, see section 6.2 of [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).</span></span>

 

## <a name="registry-values"></a><span data-ttu-id="da819-116">Valores do registro</span><span class="sxs-lookup"><span data-stu-id="da819-116">Registry Values</span></span>

<span data-ttu-id="da819-117">Os seguintes valores de registro de método de autenticador são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="da819-117">The following authenticator method registry values are required.</span></span>

-   [<span data-ttu-id="da819-118">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="da819-118">AuthenticatorDllPath</span></span>](#authenticatordllpath)
-   [<span data-ttu-id="da819-119">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="da819-119">AuthenticatorFriendlyName</span></span>](#authenticatorfriendlyname)

<span data-ttu-id="da819-120">Além dos valores de registro acima, o valor do registro do método autenticador a seguir é recomendado.</span><span class="sxs-lookup"><span data-stu-id="da819-120">Besides the above registry values, the following authenticator method registry value is recommended.</span></span>

-   [<span data-ttu-id="da819-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da819-121">Properties</span></span>](#properties)

<span data-ttu-id="da819-122">Os valores de registro do método de autenticador restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="da819-122">The remaining authenticator method registry values are optional.</span></span>

-   [<span data-ttu-id="da819-123">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="da819-123">ConfigCLSID</span></span>](#configclsid)
-   [<span data-ttu-id="da819-124">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="da819-124">StandaloneSupported</span></span>](#standalonesupported)

## <a name="authenticatordllpath"></a><span data-ttu-id="da819-125">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="da819-125">AuthenticatorDllPath</span></span>



| <span data-ttu-id="da819-126">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="da819-126">Constant Value</span></span> | <span data-ttu-id="da819-127">AuthenticatorDllPath</span><span class="sxs-lookup"><span data-stu-id="da819-127">AuthenticatorDllPath</span></span>                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da819-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="da819-128">Type</span></span>           | <span data-ttu-id="da819-129">REG \_ expande \_ sz</span><span class="sxs-lookup"><span data-stu-id="da819-129">REG\_EXPAND\_SZ</span></span>                                                                                               |
| <span data-ttu-id="da819-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="da819-130">Description</span></span>    | <span data-ttu-id="da819-131">O caminho para a DLL do método de autenticador EAP.</span><span class="sxs-lookup"><span data-stu-id="da819-131">The path to the EAP authenticator method DLL.</span></span> <span data-ttu-id="da819-132">Por exemplo,% SystemRoot% \\ System32 \\ &lt; nome \_ de \_ dll &gt; . dll.</span><span class="sxs-lookup"><span data-stu-id="da819-132">For example, %SystemRoot%\\system32\\&lt;name\_of\_DLL&gt;.dll.</span></span> |



 

## <a name="authenticatorfriendlyname"></a><span data-ttu-id="da819-133">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="da819-133">AuthenticatorFriendlyName</span></span>



| <span data-ttu-id="da819-134">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="da819-134">Constant Value</span></span> | <span data-ttu-id="da819-135">AuthenticatorFriendlyName</span><span class="sxs-lookup"><span data-stu-id="da819-135">AuthenticatorFriendlyName</span></span>                                                          |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da819-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="da819-136">Type</span></span>           | <span data-ttu-id="da819-137">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="da819-137">REG\_SZ</span></span>                                                                            |
| <span data-ttu-id="da819-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="da819-138">Description</span></span>    | <span data-ttu-id="da819-139">Cadeia de caracteres que contém o nome amigável (exibição) para o método de autenticador EAP.</span><span class="sxs-lookup"><span data-stu-id="da819-139">String that contains the friendly (display) name for the EAP authenticator method.</span></span> |



 

## <a name="configclsid"></a><span data-ttu-id="da819-140">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="da819-140">ConfigCLSID</span></span>



| <span data-ttu-id="da819-141">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="da819-141">Constant Value</span></span> | <span data-ttu-id="da819-142">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="da819-142">ConfigCLSID</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da819-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="da819-143">Type</span></span>           | <span data-ttu-id="da819-144">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="da819-144">REG\_SZ</span></span>                                                                                                                               |
| <span data-ttu-id="da819-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="da819-145">Description</span></span>    | <span data-ttu-id="da819-146">Cadeia de caracteres que contém o GUID de classe de configuração para esse método autenticador, no formato {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span><span class="sxs-lookup"><span data-stu-id="da819-146">String that contains the configuration class GUID for this authenticator method, in the format {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</span></span> |



 

## <a name="properties"></a><span data-ttu-id="da819-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da819-147">Properties</span></span>



| <span data-ttu-id="da819-148">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="da819-148">Constant Value</span></span> | <span data-ttu-id="da819-149">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da819-149">Properties</span></span>                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da819-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="da819-150">Type</span></span>           | <span data-ttu-id="da819-151">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="da819-151">REG\_DWORD</span></span>                                                                                                                                                  |
| <span data-ttu-id="da819-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="da819-152">Description</span></span>    | <span data-ttu-id="da819-153">Os bits no DWORD são definidos para indicar suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="da819-153">Bits in the DWORD are set to indicate support for the property.</span></span> <span data-ttu-id="da819-154">Para obter uma lista de valores com suporte, consulte [**Propriedades do método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="da819-154">For a list of supported values, see [**EAP Method Properties**](eap-method-properties.md).</span></span> |



 

## <a name="standalonesupported"></a><span data-ttu-id="da819-155">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="da819-155">StandaloneSupported</span></span>



| <span data-ttu-id="da819-156">Valor Constante</span><span class="sxs-lookup"><span data-stu-id="da819-156">Constant Value</span></span> | <span data-ttu-id="da819-157">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="da819-157">StandaloneSupported</span></span>                                             |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="da819-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="da819-158">Type</span></span>           | <span data-ttu-id="da819-159">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="da819-159">REG\_DWORD</span></span>                                                      |
| <span data-ttu-id="da819-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="da819-160">Description</span></span>    | <span data-ttu-id="da819-161">0 se esse for um método de autenticador autônomo; 1 se não for.</span><span class="sxs-lookup"><span data-stu-id="da819-161">0 if this is a standalone authenticator method; 1 if it is not.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="da819-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da819-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da819-163">Chaves do registro do método de par EAP</span><span class="sxs-lookup"><span data-stu-id="da819-163">EAP Peer Method Registry Keys</span></span>](eap-peer-method-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="da819-164">Configuração do registro para tipos de EAP expandidos</span><span class="sxs-lookup"><span data-stu-id="da819-164">Registry Configuration for Expanded EAP Types</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="da819-165">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="da819-165">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="da819-166">RFC 3748</span><span class="sxs-lookup"><span data-stu-id="da819-166">RFC 3748</span></span>](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




