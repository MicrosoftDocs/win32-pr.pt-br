---
title: Classe Win32_TSLicenseServer
description: Fornece métodos e propriedades para exibir e configurar o licenciamento de Área de Trabalho Remota (Licenciamento RD) em um servidor de licença Área de Trabalho Remota.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918727"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="ef0b4-105">\_Classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="ef0b4-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="ef0b4-106">Fornece métodos e propriedades para exibir e configurar o licenciamento de Área de Trabalho Remota (Licenciamento RD) em um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0b4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef0b4-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="ef0b4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ef0b4-108">Members</span></span>

<span data-ttu-id="ef0b4-109">A classe **Win32 \_ TSLicenseServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ef0b4-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="ef0b4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef0b4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef0b4-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef0b4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef0b4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef0b4-112">Methods</span></span>

<span data-ttu-id="ef0b4-113">A classe **Win32 \_ TSLicenseServer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="ef0b4-114">Método</span><span class="sxs-lookup"><span data-stu-id="ef0b4-114">Method</span></span>                                                                                   | <span data-ttu-id="ef0b4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef0b4-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef0b4-116">**ActivateServer**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="ef0b4-117">Ativa o Área de Trabalho Remota servidor de licença usando uma ID de servidor de licença de Área de Trabalho Remota que é obtida pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="ef0b4-118">**ActivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="ef0b4-119">Ativa a Área de Trabalho Remota servidor de licença automaticamente pela Internet.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="ef0b4-120">As propriedades **FirstName**, **LastName**, **Company** e **CountryRegion** não devem estar vazias quando esse método for chamado ou o método falhará.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="ef0b4-121">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="ef0b4-122">Adiciona o Área de Trabalho Remota servidor de licença ao grupo Área de Trabalho Remota servidores de licença em um controlador de domínio no mesmo domínio que o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="ef0b4-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="ef0b4-124">Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="ef0b4-125">**CreateTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="ef0b4-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-126">This method is not supported.</span></span><br/> <span data-ttu-id="ef0b4-127">**Windows server 2008 R2 e Windows server 2008:** Cria o grupo local computadores Terminal Server no Área de Trabalho Remota servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="ef0b4-128">**DeactivateServer**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="ef0b4-129">Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ef0b4-130">**DeactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="ef0b4-131">Desativa o servidor de licença Área de Trabalho Remota pela Internet.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="ef0b4-132">As propriedades **FirstName** e **LastName** não devem estar vazias quando esse método for chamado ou o método apresentar falha.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="ef0b4-133">**GetActivationStatus**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="ef0b4-134">Recupera o status de ativação atual.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="ef0b4-135">**GetLicenseServerId**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="ef0b4-136">Recupera uma Área de Trabalho Remota ID do servidor de licença se o servidor estiver ativado no momento.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="ef0b4-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="ef0b4-138">Recupera se o servidor de licença Área de Trabalho Remota é membro do grupo de servidores de licença Área de Trabalho Remota em um controlador de domínio em um determinado domínio.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="ef0b4-139">**IsLSonDC**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="ef0b4-140">Recupera se o Licenciamento RD está instalado em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="ef0b4-141">**IsLSPreventUpgradeGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="ef0b4-142">Recupera se a configuração da política de grupo "impedir atualização de licença" está habilitada no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="ef0b4-143">**IsLSPublished**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="ef0b4-144">Recupera se o servidor de licença Área de Trabalho Remota está publicado no Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ef0b4-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="ef0b4-145">**IsLSRegisteredToSCP**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="ef0b4-146">Recupera se o servidor de licença Área de Trabalho Remota está registrado como um ponto de conexão de serviço no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="ef0b4-147">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="ef0b4-148">Recupera se a configuração da política de grupo "grupo de segurança do servidor de licenças" está habilitada no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="ef0b4-149">**IsSecureAccessAllowed**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="ef0b4-150">Recupera se um servidor de Host da Sessão RD tem permissão para solicitar Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS CALs) do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="ef0b4-151">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="ef0b4-152">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-152">This method is not supported.</span></span><br/> <span data-ttu-id="ef0b4-153">**Windows server 2008 R2 e Windows server 2008:** Recupera se o grupo local computadores Terminal Server existe no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="ef0b4-154">**IsTSinTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="ef0b4-155">Recupera se um servidor de Host da Sessão RD é membro do grupo local de computadores Terminal Server no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="ef0b4-156">**PublishLS**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="ef0b4-157">Publica o servidor de licença Área de Trabalho Remota no AD DS.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="ef0b4-158">**ReactivateServer**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="ef0b4-159">Reativa o servidor de licença Área de Trabalho Remota usando uma nova ID de servidor de licença de Área de Trabalho Remota que é obtida pelo telefone ou pela Internet.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="ef0b4-160">**ReactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="ef0b4-161">Reativa o servidor de licença Área de Trabalho Remota pela Internet.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="ef0b4-162">As propriedades **FirstName** e **LastName** não devem estar vazias quando esse método for chamado ou o método apresentar falha.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="ef0b4-163">**RegisterLSToSCP**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="ef0b4-164">Registra o servidor de licença de Área de Trabalho Remota como um ponto de conexão de serviço no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="ef0b4-165">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="ef0b4-166">Remove o Área de Trabalho Remota servidor de licença do grupo Área de Trabalho Remota servidores de licenças em um controlador de domínio no mesmo domínio que o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="ef0b4-167">**RemoveTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="ef0b4-168">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-168">This method is not supported.</span></span><br/> <span data-ttu-id="ef0b4-169">**Windows server 2008 R2 e Windows server 2008:** Remove o grupo local computadores Terminal Server do Área de Trabalho Remota servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="ef0b4-170">**UnpublishLS**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="ef0b4-171">Cancelar a publicação de um servidor de licença Área de Trabalho Remota do AD DS.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="ef0b4-172">**UnRegisterLSFromSCP**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="ef0b4-173">Remove o servidor de licença Área de Trabalho Remota como um ponto de conexão de serviço no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="ef0b4-174">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef0b4-174">Properties</span></span>

<span data-ttu-id="ef0b4-175">A classe **Win32 \_ TSLicenseServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef0b4-176">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-179">Endereço do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-180">Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="ef0b4-181">(Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-182">**Cidade**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-185">Cidade do contato para Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-186">Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="ef0b4-187">(Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-188">**Empresa**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-191">Empresa do contato para Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-192">Essa propriedade é usada (e obrigatória) quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-193">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-195">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-196">País/região do contato para Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-197">Essa propriedade é usada (e obrigatória) quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0b4-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-201">Caminho do banco de dados de licenciamento do RDS.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-202">**Email**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-204">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-205">Endereço de email do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-206">Essa propriedade é usada quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="ef0b4-207">(Essa propriedade é opcional para essas chamadas de método.)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-208">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-211">Nome do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-212">Essa propriedade é usada (e obrigatória) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-213">**Sobrenome**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-215">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-216">Sobrenome do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-217">Essa propriedade é usada (e obrigatória) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-221">Unidade organizacional do contato para Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-222">Essa propriedade é usada quando o [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="ef0b4-223">(Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-227">Código postal do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-228">Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="ef0b4-229">(Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0b4-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-233">ID do produto do servidor de licença de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-235">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0b4-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-237">Descreve o escopo de licenciamento para o servidor de licença Área de Trabalho Remota dentro da organização.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="ef0b4-238">0</span><span class="sxs-lookup"><span data-stu-id="ef0b4-238">0</span></span>
</dt> <dd>

<span data-ttu-id="ef0b4-239">Host da Sessão RD servidores no mesmo grupo de trabalho podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-240">1</span><span class="sxs-lookup"><span data-stu-id="ef0b4-240">1</span></span>
</dt> <dd>

<span data-ttu-id="ef0b4-241">Host da Sessão RD servidores no mesmo domínio podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-242">2</span><span class="sxs-lookup"><span data-stu-id="ef0b4-242">2</span></span>
</dt> <dd>

<span data-ttu-id="ef0b4-243">Host da Sessão RD servidores de vários domínios na mesma floresta podem descobrir o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b4-244">**State**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-246">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ef0b4-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-247">Estado do contato para o Licenciamento RD.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="ef0b4-248">Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="ef0b4-249">(Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)</span><span class="sxs-lookup"><span data-stu-id="ef0b4-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-250">**Versão**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0b4-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-253">Versão do servidor de licença do Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b4-254">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b4-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b4-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ef0b4-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b4-257">Número de versão do servidor de licença de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef0b4-258">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef0b4-258">Remarks</span></span>

<span data-ttu-id="ef0b4-259">Essa classe é uma classe [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e pode ter apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="ef0b4-260">Todos os métodos contidos nessa classe são estáticos.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="ef0b4-261">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="ef0b4-262">Se o chamador não for um membro do grupo Administradores, as propriedades retornadas estarão vazias.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="ef0b4-263">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ef0b4-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ef0b4-264">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ef0b4-265">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ef0b4-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ef0b4-266">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ef0b4-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0b4-267">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0b4-267">Requirements</span></span>



| <span data-ttu-id="ef0b4-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0b4-268">Requirement</span></span> | <span data-ttu-id="ef0b4-269">Valor</span><span class="sxs-lookup"><span data-stu-id="ef0b4-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0b4-270">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0b4-270">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0b4-271">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ef0b4-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ef0b4-272">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0b4-272">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0b4-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef0b4-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ef0b4-274">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef0b4-274">Namespace</span></span><br/>                | <span data-ttu-id="ef0b4-275">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ef0b4-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ef0b4-276">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0b4-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0b4-277"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b4-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0b4-278">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0b4-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0b4-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b4-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0b4-280">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef0b4-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0b4-281">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="ef0b4-282">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="ef0b4-283">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="ef0b4-284">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="ef0b4-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

