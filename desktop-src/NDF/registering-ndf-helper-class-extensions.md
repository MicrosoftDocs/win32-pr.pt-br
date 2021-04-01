---
title: Registrando extensões de classe auxiliar NDF
description: Cada extensão de classe auxiliar tem um número de chaves do registro associadas a ela. Algumas chaves são exigidas pelo COM e algumas chaves são exigidas pelo NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637292"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="02d85-104">Registrando extensões de classe auxiliar NDF</span><span class="sxs-lookup"><span data-stu-id="02d85-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="02d85-105">Cada extensão de classe auxiliar tem um número de chaves do registro associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="02d85-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="02d85-106">Algumas chaves são exigidas pelo COM e algumas chaves são exigidas pelo NDF.</span><span class="sxs-lookup"><span data-stu-id="02d85-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="02d85-107">Chaves do registro COM</span><span class="sxs-lookup"><span data-stu-id="02d85-107">COM Registry Keys</span></span>

<span data-ttu-id="02d85-108">Extensões de classe auxiliar devem ser implementadas como servidores COM.</span><span class="sxs-lookup"><span data-stu-id="02d85-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="02d85-109">O registro COM deve ser concluído para cada extensão de classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="02d85-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="02d85-110">O CLSID do objeto, a interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) e a interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) devem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="02d85-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="02d85-111">O registro cria um número de chaves do registro relacionadas COM para a extensão de classe auxiliar NDF.</span><span class="sxs-lookup"><span data-stu-id="02d85-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="02d85-112">Chaves do registro NDF</span><span class="sxs-lookup"><span data-stu-id="02d85-112">NDF Registry Keys</span></span>

<span data-ttu-id="02d85-113">Extensões de classe auxiliar devem ser registradas antes de interagir com a estrutura de diagnóstico de rede e com outras classes auxiliares relacionadas.</span><span class="sxs-lookup"><span data-stu-id="02d85-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="02d85-114">Isso é feito preenchendo o registro.</span><span class="sxs-lookup"><span data-stu-id="02d85-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="02d85-115">O procedimento a seguir mostra como adicionar extensões de classe auxiliar ao registro.</span><span class="sxs-lookup"><span data-stu-id="02d85-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="02d85-116">Publique os nomes das classes auxiliares implementadas pela DLL e suas dependências criando uma chave para a DLL em</span><span class="sxs-lookup"><span data-stu-id="02d85-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="02d85-117">**HKLM \\ Sistema \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *vendornamename* \\ **HostDLLs** \\ *auxiliar classe dll* \\ **HelperClasses** \\ *nome da classe auxiliar*</span><span class="sxs-lookup"><span data-stu-id="02d85-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="02d85-118">Substitua *VendorName*, *dll de classe auxiliar* e *nome de classe auxiliar* por valores definidos pelo usuário, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="02d85-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="02d85-119">Valor</span><span class="sxs-lookup"><span data-stu-id="02d85-119">Value</span></span>               | <span data-ttu-id="02d85-120">Type</span><span class="sxs-lookup"><span data-stu-id="02d85-120">Type</span></span>    | <span data-ttu-id="02d85-121">Significado</span><span class="sxs-lookup"><span data-stu-id="02d85-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="02d85-122">*Nome_do_Fornecedor*</span><span class="sxs-lookup"><span data-stu-id="02d85-122">*VendorName*</span></span>        | <span data-ttu-id="02d85-123">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-123">REG\_SZ</span></span> | <span data-ttu-id="02d85-124">O nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="02d85-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="02d85-125">*DLL de classe auxiliar*</span><span class="sxs-lookup"><span data-stu-id="02d85-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="02d85-126">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-126">REG\_SZ</span></span> | <span data-ttu-id="02d85-127">Nome da DLL, sem extensão.</span><span class="sxs-lookup"><span data-stu-id="02d85-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="02d85-128">*Nome da classe auxiliar*</span><span class="sxs-lookup"><span data-stu-id="02d85-128">*Helper Class Name*</span></span> | <span data-ttu-id="02d85-129">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-129">REG\_SZ</span></span> | <span data-ttu-id="02d85-130">O nome da classe auxiliar na qual a classe auxiliar atual é dependente.</span><span class="sxs-lookup"><span data-stu-id="02d85-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="02d85-131">Em cada chave de *nome de classe auxiliar* , publique as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="02d85-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="02d85-132">Valor</span><span class="sxs-lookup"><span data-stu-id="02d85-132">Value</span></span>         | <span data-ttu-id="02d85-133">Type</span><span class="sxs-lookup"><span data-stu-id="02d85-133">Type</span></span>       | <span data-ttu-id="02d85-134">Significado</span><span class="sxs-lookup"><span data-stu-id="02d85-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="02d85-135">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="02d85-135">**CLSID**</span></span>     | <span data-ttu-id="02d85-136">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-136">REG\_SZ</span></span>    | <span data-ttu-id="02d85-137">Uma cadeia de caracteres que contém a ID de classe COM da classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="02d85-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="02d85-138">**Versão**</span><span class="sxs-lookup"><span data-stu-id="02d85-138">**Version**</span></span>   | <span data-ttu-id="02d85-139">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-139">REG\_SZ</span></span>    | <span data-ttu-id="02d85-140">Uma cadeia de caracteres contém as versões principal e secundária da classe auxiliar no formato <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="02d85-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="02d85-141">**Checked**</span><span class="sxs-lookup"><span data-stu-id="02d85-141">**Published**</span></span> | <span data-ttu-id="02d85-142">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="02d85-142">REG\_DWORD</span></span> | <span data-ttu-id="02d85-143">Um valor de 1 significa que essa classe auxiliar deve ser invocada diretamente do cliente de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="02d85-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="02d85-144">0 significa que ele pode ser chamado somente de outra classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="02d85-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="02d85-145">**Pai**</span><span class="sxs-lookup"><span data-stu-id="02d85-145">**Parent**</span></span>    | <span data-ttu-id="02d85-146">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="02d85-146">REG\_SZ</span></span>    | <span data-ttu-id="02d85-147">Uma cadeia de caracteres que nomeia a classe auxiliar extensível da Microsoft que está sendo estendida.</span><span class="sxs-lookup"><span data-stu-id="02d85-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="02d85-148">Para cada classe auxiliar, publique a lista de atributos correspondentes criando uma chave em</span><span class="sxs-lookup"><span data-stu-id="02d85-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="02d85-149">**HKLM \\ Sistema \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *nome_do_fornecedorname* \\ **HostDLLs** \\ *auxiliar classe dll* \\ **HelperClasses** \\ *nome da classe auxiliar* \\ **matchattributes**</span><span class="sxs-lookup"><span data-stu-id="02d85-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="02d85-150">A chave deve conter um ou mais valores (um por atributo) do seguinte tipo.</span><span class="sxs-lookup"><span data-stu-id="02d85-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="02d85-151">Valor</span><span class="sxs-lookup"><span data-stu-id="02d85-151">Value</span></span>             | <span data-ttu-id="02d85-152">Type</span><span class="sxs-lookup"><span data-stu-id="02d85-152">Type</span></span>                             | <span data-ttu-id="02d85-153">Significado</span><span class="sxs-lookup"><span data-stu-id="02d85-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="02d85-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="02d85-154">**AttributeName**</span></span> | <span data-ttu-id="02d85-155">REG. reg do registro \_ \| \_ DWORD \| \_</span><span class="sxs-lookup"><span data-stu-id="02d85-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="02d85-156">Um valor que conclui o par de nome e valor de um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="02d85-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




