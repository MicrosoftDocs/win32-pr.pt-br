---
description: Remoção da reflexão do registro do Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Remoção da reflexão do registro do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116254"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="bae9a-103">Remoção da reflexão do registro do Windows</span><span class="sxs-lookup"><span data-stu-id="bae9a-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="bae9a-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="bae9a-104">Platform</span></span>

<span data-ttu-id="bae9a-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="bae9a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="bae9a-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bae9a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="bae9a-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="bae9a-107">Feature Impact</span></span>

 <span data-ttu-id="bae9a-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="bae9a-108">**Severity** - Low</span></span>  
<span data-ttu-id="bae9a-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="bae9a-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="bae9a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bae9a-110">Description</span></span>

<span data-ttu-id="bae9a-111">O processo de reflexão do registro copia chaves e valores do registro entre duas exibições do registro para mantê-las em sincronia. Nas instalações anteriores de 64 bits do Windows, o processo refletiu um subconjunto das chaves do registro redirecionadas entre as exibições de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bae9a-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="bae9a-112">No entanto, a implementação disso causou algumas inconsistências no estado do registro.</span><span class="sxs-lookup"><span data-stu-id="bae9a-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="bae9a-113">(Para obter detalhes sobre a reflexão do registro, consulte o artigo correspondente do MSDN na seção *links para outros recursos* abaixo.)</span><span class="sxs-lookup"><span data-stu-id="bae9a-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="bae9a-114">A partir do Windows 7, removemos completamente a reflexão do registro e mesclamos as chaves que costumava ser refletidas:</span><span class="sxs-lookup"><span data-stu-id="bae9a-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="bae9a-115">HKEY \_ local \_ Machine \\ software \\ classes</span><span class="sxs-lookup"><span data-stu-id="bae9a-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="bae9a-116">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ com3</span><span class="sxs-lookup"><span data-stu-id="bae9a-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="bae9a-117">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="bae9a-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="bae9a-118">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="bae9a-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="bae9a-119">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="bae9a-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="bae9a-120">HKey \_ usuários \\ \* \\ classes de software \\</span><span class="sxs-lookup"><span data-stu-id="bae9a-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="bae9a-121">\_Classes de usuários hKey \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="bae9a-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="bae9a-122">Efetivamente, isso fornece o mesmo comportamento de reflexão, pois as alterações a essas chaves imediatamente estão disponíveis para aplicativos de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bae9a-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="bae9a-123">As chaves que foram refletidas condicionalmente permanecem divididas:</span><span class="sxs-lookup"><span data-stu-id="bae9a-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="bae9a-124">HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="bae9a-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="bae9a-125">HKEY \_ local \_ Machine \\ software \\ classes \\ interface</span><span class="sxs-lookup"><span data-stu-id="bae9a-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="bae9a-126">O hKey \_ Users \\ \* \\ classes de software \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="bae9a-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="bae9a-127">HKey \_ Users \\ \* \\ \\ interface classes de software \\</span><span class="sxs-lookup"><span data-stu-id="bae9a-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="bae9a-128">\_CLSID de \\ \* \_ classes \\ de usuários hKey</span><span class="sxs-lookup"><span data-stu-id="bae9a-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="bae9a-129">\_Interface de \\ \* \_ classes \\ de usuários hKey</span><span class="sxs-lookup"><span data-stu-id="bae9a-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="bae9a-130">Eles são usados para manter os dados que não devem ser compartilhados entre aplicativos de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bae9a-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="bae9a-131">Manifestação</span><span class="sxs-lookup"><span data-stu-id="bae9a-131">Manifestation</span></span>

<span data-ttu-id="bae9a-132">As chaves CLSID e de interface da lista acima não são mais refletidas enquanto ainda são redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="bae9a-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="bae9a-133">Embora esse seja o comportamento desejado na maioria dos casos, é possível que os aplicativos possam assumir uma dependência do comportamento refletido no vista.</span><span class="sxs-lookup"><span data-stu-id="bae9a-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="bae9a-134">As funções que permitem que os aplicativos controlem a reflexão (RegDisableReflectionKey e RegEnableReflectionKey) são não Ops no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bae9a-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="bae9a-135">Mitigação do impacto</span><span class="sxs-lookup"><span data-stu-id="bae9a-135">Mitigation of Impact</span></span>

<span data-ttu-id="bae9a-136">COM é o principal consumidor de reflexão de registro.</span><span class="sxs-lookup"><span data-stu-id="bae9a-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="bae9a-137">COM e outros consumidores foram atualizados para acomodar essa alteração.</span><span class="sxs-lookup"><span data-stu-id="bae9a-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="bae9a-138">Essa alteração não afeta os aplicativos que usam APIs COM padrão.</span><span class="sxs-lookup"><span data-stu-id="bae9a-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="bae9a-139">Solução</span><span class="sxs-lookup"><span data-stu-id="bae9a-139">Solution</span></span>

<span data-ttu-id="bae9a-140">Aplique uma das opções a seguir se você estiver contando com a reflexão do registro para sincronizar as exibições de 32 bits e 64 bits:</span><span class="sxs-lookup"><span data-stu-id="bae9a-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="bae9a-141">Criar chaves em ambas as exibições explicitamente durante a instalação</span><span class="sxs-lookup"><span data-stu-id="bae9a-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="bae9a-142">Mover as chaves para fora do escopo das chaves refletidas</span><span class="sxs-lookup"><span data-stu-id="bae9a-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="bae9a-143">Verificar as duas exibições do registro ao consultar uma chave refletida</span><span class="sxs-lookup"><span data-stu-id="bae9a-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="bae9a-144">**Observação:** CHAVE \_ \_ 32KEY de WOW64 e \_ sinalizadores de 64KEY de WOW64 principais \_ não podem ser combinados</span><span class="sxs-lookup"><span data-stu-id="bae9a-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="bae9a-145">Aplique uma das opções a seguir se você estiver contando com as funções RegDisableReflectionKey para desabilitar a reflexão do registro:</span><span class="sxs-lookup"><span data-stu-id="bae9a-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="bae9a-146">Criar chaves em ambas as exibições explicitamente durante a instalação</span><span class="sxs-lookup"><span data-stu-id="bae9a-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="bae9a-147">Mover as chaves para fora do escopo das chaves refletidas</span><span class="sxs-lookup"><span data-stu-id="bae9a-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="bae9a-148">Usar subchaves específicas da plataforma (como x86, AMD64 e IA64) para separar dados específicos de um bit de bits</span><span class="sxs-lookup"><span data-stu-id="bae9a-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="bae9a-149">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="bae9a-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="bae9a-150">Artigo de reflexo do registro</span><span class="sxs-lookup"><span data-stu-id="bae9a-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="bae9a-151">Lista de chaves redirecionadas no artigo redirecionador do registro</span><span class="sxs-lookup"><span data-stu-id="bae9a-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="bae9a-152">Práticas recomendadas para o WOW64</span><span class="sxs-lookup"><span data-stu-id="bae9a-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="bae9a-153">Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="bae9a-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
