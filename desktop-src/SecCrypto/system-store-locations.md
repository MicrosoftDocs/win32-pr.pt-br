---
description: Um repositório do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Locais de armazenamento do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921848"
---
# <a name="system-store-locations"></a><span data-ttu-id="e5869-103">Locais de armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-103">System Store Locations</span></span>

<span data-ttu-id="e5869-104">Um repositório do sistema é uma coleção que consiste em um ou mais armazenamentos irmãos físicos.</span><span class="sxs-lookup"><span data-stu-id="e5869-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="e5869-105">Para cada repositório do sistema, há repositórios irmãos físicos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e5869-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="e5869-106">Depois de abrir um repositório do sistema, como meu no \_ sistema CERT \_ \_ \_ do usuário atual, o provedor da loja chama [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada um dos repositórios físicos na coleção de armazenamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="e5869-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="e5869-107">No processo aberto, cada um desses repositórios físicos é adicionado à coleção de armazenamento do sistema usando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="e5869-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="e5869-108">Todos os certificados nesses repositórios físicos estão disponíveis por meio da coleção de armazenamento do sistema lógico.</span><span class="sxs-lookup"><span data-stu-id="e5869-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="e5869-109">Para cada local de repositório do sistema, os armazenamentos de sistemas predefinidos são:</span><span class="sxs-lookup"><span data-stu-id="e5869-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="e5869-110">MY</span><span class="sxs-lookup"><span data-stu-id="e5869-110">MY</span></span>
-   <span data-ttu-id="e5869-111">Root</span><span class="sxs-lookup"><span data-stu-id="e5869-111">Root</span></span>
-   <span data-ttu-id="e5869-112">Confiar</span><span class="sxs-lookup"><span data-stu-id="e5869-112">Trust</span></span>
-   <span data-ttu-id="e5869-113">AC</span><span class="sxs-lookup"><span data-stu-id="e5869-113">CA</span></span>

<span data-ttu-id="e5869-114">No \_ usuário atual do repositório do sistema de certificados \_ \_ \_ , há também um repositório UserDS predefinido.</span><span class="sxs-lookup"><span data-stu-id="e5869-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="e5869-115">Um repositório de cartão inteligente está planejado para esse local.</span><span class="sxs-lookup"><span data-stu-id="e5869-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="e5869-116">Aqui estão as lojas de sistema seguidas por comentários adicionais:</span><span class="sxs-lookup"><span data-stu-id="e5869-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="e5869-117">\_ \_ usuário atual do repositório do sistema de \_ certificados \_</span><span class="sxs-lookup"><span data-stu-id="e5869-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="e5869-118">\_ \_ máquina local do repositório do sistema de \_ certificados \_</span><span class="sxs-lookup"><span data-stu-id="e5869-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="e5869-119">\_ \_ serviço atual do repositório do sistema de \_ CERT. \_</span><span class="sxs-lookup"><span data-stu-id="e5869-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="e5869-120">\_serviços de \_ loja do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="e5869-121">\_usuários do \_ repositório do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="e5869-122">\_política de \_ \_ grupo de usuário atual do sistema \_ de certificado \_</span><span class="sxs-lookup"><span data-stu-id="e5869-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="e5869-123">\_política de \_ \_ grupo do computador local do sistema \_ de CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="e5869-124">\_máquina local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="e5869-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="e5869-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5869-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="e5869-126">\_ \_ usuário atual do repositório do sistema de \_ certificados \_</span><span class="sxs-lookup"><span data-stu-id="e5869-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="e5869-127">Os armazenamentos \_ \_ do sistema do usuário atual do repositório do sistema \_ de certificados \_ estão no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="e5869-128">Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="e5869-129">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-129">System store</span></span> | <span data-ttu-id="e5869-130">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="e5869-131">MY</span><span class="sxs-lookup"><span data-stu-id="e5869-131">MY</span></span>           | <span data-ttu-id="e5869-132">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-132">.Default</span></span>                                                 |
| <span data-ttu-id="e5869-133">Root</span><span class="sxs-lookup"><span data-stu-id="e5869-133">Root</span></span>         | <span data-ttu-id="e5869-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="e5869-135">. Smart</span><span class="sxs-lookup"><span data-stu-id="e5869-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="e5869-136">Confiar</span><span class="sxs-lookup"><span data-stu-id="e5869-136">Trust</span></span>        | <span data-ttu-id="e5869-137">. Padrão. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="e5869-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="e5869-138">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-139">AC</span><span class="sxs-lookup"><span data-stu-id="e5869-139">CA</span></span>           | <span data-ttu-id="e5869-140">. Padrão. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="e5869-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="e5869-141">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-142">UserDS</span><span class="sxs-lookup"><span data-stu-id="e5869-142">UserDS</span></span>       | <span data-ttu-id="e5869-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="e5869-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="e5869-144">\_ \_ máquina local do repositório do sistema de \_ certificados \_</span><span class="sxs-lookup"><span data-stu-id="e5869-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="e5869-145">Os armazenamentos do sistema \_ \_ do computador local do repositório do sistema \_ de certificados \_ estão no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="e5869-146">Os repositórios físicos predefinidos são associados a esses repositórios de sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="e5869-147">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-147">System store</span></span> | <span data-ttu-id="e5869-148">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5869-149">MY</span><span class="sxs-lookup"><span data-stu-id="e5869-149">MY</span></span>           | <span data-ttu-id="e5869-150">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="e5869-151">Root</span><span class="sxs-lookup"><span data-stu-id="e5869-151">Root</span></span>         | <span data-ttu-id="e5869-152">. Padrão. AuthRoot</span><span class="sxs-lookup"><span data-stu-id="e5869-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="e5869-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="e5869-153">.GroupPolicy</span></span><br/> <span data-ttu-id="e5869-154">. Porte</span><span class="sxs-lookup"><span data-stu-id="e5869-154">.Enterprise</span></span><br/> <span data-ttu-id="e5869-155">. Smart</span><span class="sxs-lookup"><span data-stu-id="e5869-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="e5869-156">Confiar</span><span class="sxs-lookup"><span data-stu-id="e5869-156">Trust</span></span>        | <span data-ttu-id="e5869-157">. Padrão. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="e5869-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="e5869-158">. Porte</span><span class="sxs-lookup"><span data-stu-id="e5869-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="e5869-159">AC</span><span class="sxs-lookup"><span data-stu-id="e5869-159">CA</span></span>           | <span data-ttu-id="e5869-160">. Padrão. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="e5869-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="e5869-161">. Porte</span><span class="sxs-lookup"><span data-stu-id="e5869-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="e5869-162">\_ \_ serviço atual do repositório do sistema de \_ CERT. \_</span><span class="sxs-lookup"><span data-stu-id="e5869-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="e5869-163">\_ \_ \_ \_ Os armazenamentos do sistema de serviço atual do repositório do sistema de certificados estão no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="e5869-164">Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="e5869-165">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-165">System store</span></span> | <span data-ttu-id="e5869-166">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="e5869-167">MY</span><span class="sxs-lookup"><span data-stu-id="e5869-167">MY</span></span>           | <span data-ttu-id="e5869-168">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-168">.Default</span></span>                         |
| <span data-ttu-id="e5869-169">Root</span><span class="sxs-lookup"><span data-stu-id="e5869-169">Root</span></span>         | <span data-ttu-id="e5869-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-171">Confiar</span><span class="sxs-lookup"><span data-stu-id="e5869-171">Trust</span></span>        | <span data-ttu-id="e5869-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-173">AC</span><span class="sxs-lookup"><span data-stu-id="e5869-173">CA</span></span>           | <span data-ttu-id="e5869-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="e5869-175">\_serviços de \_ loja do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="e5869-176">\_ \_ \_ Os serviços de repositório do sistema de certificados são armazenados no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="e5869-177">Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="e5869-178">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-178">System store</span></span>       | <span data-ttu-id="e5869-179">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="e5869-180">Nome do \\ meu</span><span class="sxs-lookup"><span data-stu-id="e5869-180">ServiceName\\MY</span></span>    | <span data-ttu-id="e5869-181">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-181">.Default</span></span>                         |
| <span data-ttu-id="e5869-182">Raiz do ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="e5869-182">ServiceName\\Root</span></span>  | <span data-ttu-id="e5869-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-184">Confiança do ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="e5869-184">ServiceName\\Trust</span></span> | <span data-ttu-id="e5869-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-186">AC do ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="e5869-186">ServiceName\\CA</span></span>    | <span data-ttu-id="e5869-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="e5869-188">\_usuários do \_ repositório do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="e5869-189">\_ \_ Os usuários do repositório do sistema de certificados \_ armazenam o sistema no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="e5869-190">Os repositórios físicos predefinidos associados a esses armazenamentos do sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="e5869-191">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-191">System store</span></span>  | <span data-ttu-id="e5869-192">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="e5869-193">userid \\ My</span><span class="sxs-lookup"><span data-stu-id="e5869-193">userid\\MY</span></span>    | <span data-ttu-id="e5869-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-195">raiz da userid \\</span><span class="sxs-lookup"><span data-stu-id="e5869-195">userid\\Root</span></span>  | <span data-ttu-id="e5869-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-197">confiança de userid \\</span><span class="sxs-lookup"><span data-stu-id="e5869-197">userid\\Trust</span></span> | <span data-ttu-id="e5869-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="e5869-199">\\AC da userid</span><span class="sxs-lookup"><span data-stu-id="e5869-199">userid\\CA</span></span>    | <span data-ttu-id="e5869-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="e5869-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="e5869-201">\_política de \_ \_ grupo de usuário atual do sistema \_ de certificado \_</span><span class="sxs-lookup"><span data-stu-id="e5869-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="e5869-202">\_ \_ \_ A política de grupo do usuário atual do sistema de certificados \_ \_ armazena o sistema no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="e5869-203">\_política de \_ \_ grupo do computador local do sistema \_ de CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="e5869-204">\_ \_ \_ A política de grupo do computador local do sistema de CERT \_ \_ repositórios do sistema está no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="e5869-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="e5869-205">\_máquina local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="e5869-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="e5869-206">O \_ computador local do repositório do sistema de certificados \_ \_ \_ \_ Enterprise contém certificados compartilhados entre domínios na empresa e baixados do diretório empresarial global.</span><span class="sxs-lookup"><span data-stu-id="e5869-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="e5869-207">Para sincronizar a Enterprise Store do cliente, o diretório da empresa é sondado a cada oito horas e os certificados são baixados automaticamente em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e5869-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="e5869-208">Os repositórios físicos predefinidos associados a esses repositórios do sistema são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e5869-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="e5869-209">Armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="e5869-209">System store</span></span> | <span data-ttu-id="e5869-210">Repositório físico</span><span class="sxs-lookup"><span data-stu-id="e5869-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="e5869-211">MY</span><span class="sxs-lookup"><span data-stu-id="e5869-211">MY</span></span>           | <span data-ttu-id="e5869-212">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-212">.Default</span></span>       |
| <span data-ttu-id="e5869-213">Root</span><span class="sxs-lookup"><span data-stu-id="e5869-213">Root</span></span>         | <span data-ttu-id="e5869-214">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-214">.Default</span></span>       |
| <span data-ttu-id="e5869-215">Confiar</span><span class="sxs-lookup"><span data-stu-id="e5869-215">Trust</span></span>        | <span data-ttu-id="e5869-216">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-216">.Default</span></span>       |
| <span data-ttu-id="e5869-217">AC</span><span class="sxs-lookup"><span data-stu-id="e5869-217">CA</span></span>           | <span data-ttu-id="e5869-218">. Os</span><span class="sxs-lookup"><span data-stu-id="e5869-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="e5869-219">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5869-219">Remarks</span></span>

<span data-ttu-id="e5869-220">Repositórios físicos adicionais podem ser associados a um repositório do sistema usando o [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="e5869-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="e5869-221">O \_ \_ serviço de repositório do sistema CERT \_ e \_ os usuários do repositório do sistema de certificados \_ \_ são abertos por meio da prefixação do nome do repositório na cadeia de caracteres passada para  *pvPara* com o serviço ou nome de usuário, como ServiceName \\ **Trust** ou **.** \\ **My** padrão.</span><span class="sxs-lookup"><span data-stu-id="e5869-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="e5869-222">O local dos usuários do repositório do sistema CERT \_ \_ ou do \_ CERT System Store \_ \_ \_ podem abrir o mesmo armazenamento no \_ serviço atual do sistema de CERT ou no \_ \_ \_ usuário atual do repositório do sistema de certificados \_ \_ \_ usando o Sid ( [*identificador de segurança*](../secgloss/s-gly.md) textual) do serviço ou usuário atual.</span><span class="sxs-lookup"><span data-stu-id="e5869-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="e5869-223">Os repositórios na política de \_ grupo do usuário da loja sistema de certificados \_ \_ \_ \_ e \_ \_ \_ na política de grupo do computador local do sistema de certificados \_ \_ em uma configuração de rede são baixados para o computador cliente do modelo de política de grupo (GPT) durante a inicialização do computador ou logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="e5869-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="e5869-224">Esses armazenamentos podem ser atualizados no computador cliente após a inicialização ou o logon quando o GPT é alterado no servidor de domínio por um administrador.</span><span class="sxs-lookup"><span data-stu-id="e5869-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="e5869-225">A função [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite que um aplicativo seja notificado quando as lojas em qualquer um desses locais forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="e5869-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="e5869-226">Os seguintes locais de armazenamento do sistema podem ser abertos remotamente:</span><span class="sxs-lookup"><span data-stu-id="e5869-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="e5869-227">\_ \_ máquina local do repositório do sistema de \_ certificados \_</span><span class="sxs-lookup"><span data-stu-id="e5869-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="e5869-228">\_política de \_ \_ grupo do \_ computador local do \_ repositório \_ do sistema de certificados</span><span class="sxs-lookup"><span data-stu-id="e5869-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="e5869-229">\_serviços de \_ loja do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="e5869-230">\_usuários do \_ repositório do sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="e5869-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="e5869-231">Os locais da loja do sistema são abertos remotamente por meio da prefixação do nome do repositório na cadeia de caracteres passada para *pvPara* com o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="e5869-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="e5869-232">Exemplos de nomes de repositório do sistema remoto:</span><span class="sxs-lookup"><span data-stu-id="e5869-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="e5869-233">*ComputerName* \\ **AC**</span><span class="sxs-lookup"><span data-stu-id="e5869-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="e5869-234">\\\\*ComputerName* \\ **AC**</span><span class="sxs-lookup"><span data-stu-id="e5869-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="e5869-235">*ComputerName* \\ *ServiceName* \\ **Confiar**</span><span class="sxs-lookup"><span data-stu-id="e5869-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="e5869-236">\\\\*ComputerName* \\ *ServiceName* \\ **Confiar**</span><span class="sxs-lookup"><span data-stu-id="e5869-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
