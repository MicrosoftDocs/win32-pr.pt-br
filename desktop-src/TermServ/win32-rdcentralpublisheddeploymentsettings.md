---
title: Classe Win32_RDCentralPublishedDeploymentSettings
description: Contém as configurações de implantação usadas para gerar arquivos RDP para recursos publicados de um farm.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedDeploymentSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedDeploymentSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369868"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="f7d42-105">\_Classe Win32 RDCentralPublishedDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="f7d42-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="f7d42-106">Contém as configurações de implantação usadas para gerar arquivos RDP para recursos publicados de um farm.</span><span class="sxs-lookup"><span data-stu-id="f7d42-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="f7d42-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f7d42-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d42-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7d42-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="f7d42-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f7d42-109">Members</span></span>

<span data-ttu-id="f7d42-110">A classe **Win32 \_ RDCentralPublishedDeploymentSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7d42-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="f7d42-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7d42-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7d42-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7d42-112">Properties</span></span>

<span data-ttu-id="f7d42-113">A classe **Win32 \_ RDCentralPublishedDeploymentSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7d42-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7d42-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="f7d42-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-115">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7d42-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-117">**true** para permitir a suavização de fontes; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f7d42-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f7d42-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7d42-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f7d42-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-122">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7d42-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f7d42-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7d42-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="f7d42-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-125">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="f7d42-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-127">O certificado usado para assinar os arquivos RDP; necessariamente somente se *HasCertificate* for true.</span><span class="sxs-lookup"><span data-stu-id="f7d42-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-128">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="f7d42-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7d42-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-131">Contém a profundidade de bits de cor:</span><span class="sxs-lookup"><span data-stu-id="f7d42-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="f7d42-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="f7d42-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="f7d42-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="f7d42-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="f7d42-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="f7d42-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="f7d42-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7d42-138">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="f7d42-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-141">Contém o conteúdo do arquivo RDP correspondente às configurações personalizadas de RDP.</span><span class="sxs-lookup"><span data-stu-id="f7d42-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-142">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="f7d42-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-145">Contém o conteúdo do arquivo RDP correspondente às configurações de implantação.</span><span class="sxs-lookup"><span data-stu-id="f7d42-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="f7d42-146">Se esse parâmetro for definido, o sistema usará esse arquivo RDP e ignorará as outras configurações de RDP nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="f7d42-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-147">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f7d42-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7d42-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-150">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7d42-150">Description of the object.</span></span>

<span data-ttu-id="f7d42-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7d42-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-152">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="f7d42-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-155">O nome do farm.</span><span class="sxs-lookup"><span data-stu-id="f7d42-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-156">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="f7d42-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7d42-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-159">Contém o modo de autenticação do gateway:</span><span class="sxs-lookup"><span data-stu-id="f7d42-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="f7d42-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Senha (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="f7d42-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="f7d42-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Cartão inteligente (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="f7d42-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="f7d42-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Permitir que o usuário escolha (4)** (4)</span><span class="sxs-lookup"><span data-stu-id="f7d42-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7d42-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="f7d42-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-166">O nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d42-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-167">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="f7d42-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7d42-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-170">Descreve como o gateway é usado:</span><span class="sxs-lookup"><span data-stu-id="f7d42-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="f7d42-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Nogateway** (0)</span><span class="sxs-lookup"><span data-stu-id="f7d42-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f7d42-172">Sem gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d42-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="f7d42-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span><span class="sxs-lookup"><span data-stu-id="f7d42-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f7d42-174">Use a passagem de gateway por local.</span><span class="sxs-lookup"><span data-stu-id="f7d42-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="f7d42-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span><span class="sxs-lookup"><span data-stu-id="f7d42-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f7d42-176">Use o gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d42-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="f7d42-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span><span class="sxs-lookup"><span data-stu-id="f7d42-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f7d42-178">Detectar gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d42-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7d42-179">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="f7d42-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7d42-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-182">**true** para usar as mesmas credenciais de usuário para Gateway TS e servidor TS, quando possível; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f7d42-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-183">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="f7d42-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7d42-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-185">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-186">**true** para usar um certificado para assinar os arquivos RDP; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f7d42-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7d42-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-188">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7d42-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7d42-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-190">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="f7d42-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-191">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f7d42-191">The date the object was installed.</span></span> <span data-ttu-id="f7d42-192">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f7d42-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f7d42-193">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7d42-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-194">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f7d42-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7d42-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-197">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7d42-197">The name of the object.</span></span>

<span data-ttu-id="f7d42-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7d42-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-199">**Porta**</span><span class="sxs-lookup"><span data-stu-id="f7d42-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-200">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7d42-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-202">A porta RDP.</span><span class="sxs-lookup"><span data-stu-id="f7d42-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-203">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="f7d42-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-206">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f7d42-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-207">O alias do farm que publicou o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7d42-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-208">**Redireçãooptions**</span><span class="sxs-lookup"><span data-stu-id="f7d42-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-209">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f7d42-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-211">Opções de redirecionamento:</span><span class="sxs-lookup"><span data-stu-id="f7d42-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="f7d42-212">0</span><span class="sxs-lookup"><span data-stu-id="f7d42-212">0</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-213">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f7d42-213">None</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-214">1</span><span class="sxs-lookup"><span data-stu-id="f7d42-214">1</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-215">Unidades</span><span class="sxs-lookup"><span data-stu-id="f7d42-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-216">2</span><span class="sxs-lookup"><span data-stu-id="f7d42-216">2</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-217">Impressoras</span><span class="sxs-lookup"><span data-stu-id="f7d42-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-218">4</span><span class="sxs-lookup"><span data-stu-id="f7d42-218">4</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-219">Área de Transferência</span><span class="sxs-lookup"><span data-stu-id="f7d42-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-220">8</span><span class="sxs-lookup"><span data-stu-id="f7d42-220">8</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-221">Plug and Play</span><span class="sxs-lookup"><span data-stu-id="f7d42-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="f7d42-222">16</span><span class="sxs-lookup"><span data-stu-id="f7d42-222">16</span></span>
</dt> <dd>

<span data-ttu-id="f7d42-223">Cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="f7d42-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f7d42-224">**Status**</span><span class="sxs-lookup"><span data-stu-id="f7d42-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7d42-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7d42-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-227">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f7d42-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-228">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7d42-228">Current status of the object.</span></span> <span data-ttu-id="f7d42-229">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="f7d42-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f7d42-230">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="f7d42-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f7d42-231">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="f7d42-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f7d42-232">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="f7d42-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f7d42-233">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="f7d42-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f7d42-234">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7d42-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f7d42-235">("OK")</span><span class="sxs-lookup"><span data-stu-id="f7d42-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-236">("Erro")</span><span class="sxs-lookup"><span data-stu-id="f7d42-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-237">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="f7d42-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-238">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f7d42-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-239">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f7d42-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-240">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f7d42-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-241">("Parando")</span><span class="sxs-lookup"><span data-stu-id="f7d42-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f7d42-242">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="f7d42-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7d42-243">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="f7d42-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7d42-244">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f7d42-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f7d42-245">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f7d42-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f7d42-246">**true** para habilitar vários monitores para área de trabalho (não trilho); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f7d42-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7d42-247">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7d42-247">Requirements</span></span>



| <span data-ttu-id="f7d42-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d42-248">Requirement</span></span> | <span data-ttu-id="f7d42-249">Valor</span><span class="sxs-lookup"><span data-stu-id="f7d42-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d42-250">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d42-250">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d42-251">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f7d42-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f7d42-252">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d42-252">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d42-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7d42-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="f7d42-254">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7d42-254">Namespace</span></span><br/>                | <span data-ttu-id="f7d42-255">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f7d42-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f7d42-256">MOF</span><span class="sxs-lookup"><span data-stu-id="f7d42-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7d42-257"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7d42-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f7d42-258">DLL</span><span class="sxs-lookup"><span data-stu-id="f7d42-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7d42-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7d42-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

