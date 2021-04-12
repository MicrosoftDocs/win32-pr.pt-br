---
title: Classe Win32_TSDeploymentSettings
description: Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos de protocolo RDP (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSDeploymentSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSDeploymentSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455038"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="52867-105">\_Classe Win32 TSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="52867-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="52867-106">Define as configurações padrão que o Gerenciador RemoteApp usa ao criar arquivos de protocolo RDP (RDP).</span><span class="sxs-lookup"><span data-stu-id="52867-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="52867-107">Essas configurações não afetam nenhum aplicativo ou área de trabalho publicada.</span><span class="sxs-lookup"><span data-stu-id="52867-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="52867-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52867-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="52867-109">Membros</span><span class="sxs-lookup"><span data-stu-id="52867-109">Members</span></span>

<span data-ttu-id="52867-110">A classe **Win32 \_ TSDeploymentSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="52867-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="52867-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52867-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52867-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52867-112">Properties</span></span>

<span data-ttu-id="52867-113">A classe **Win32 \_ TSDeploymentSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="52867-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52867-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="52867-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-115">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52867-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52867-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-117">Indica se a suavização de fonte deve ser permitida.</span><span class="sxs-lookup"><span data-stu-id="52867-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="52867-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="52867-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52867-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52867-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="52867-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="52867-122">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="52867-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="52867-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52867-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52867-124">**CertificateExpiresOn**</span><span class="sxs-lookup"><span data-stu-id="52867-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-127">A data em que o certificado expira.</span><span class="sxs-lookup"><span data-stu-id="52867-127">The date that the certificate expires on.</span></span> <span data-ttu-id="52867-128">Esse valor é armazenado como um formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="52867-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="52867-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="52867-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-130">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="52867-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="52867-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-132">A impressão digital do certificado que é usado para assinar arquivos RDP.</span><span class="sxs-lookup"><span data-stu-id="52867-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="52867-133">**CertificateIssuedBy**</span><span class="sxs-lookup"><span data-stu-id="52867-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-136">Especifica a quem o certificado é emitido.</span><span class="sxs-lookup"><span data-stu-id="52867-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="52867-137">**CertificateIssuedTo**</span><span class="sxs-lookup"><span data-stu-id="52867-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-140">Especifica para quem o certificado é emitido.</span><span class="sxs-lookup"><span data-stu-id="52867-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="52867-141">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="52867-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-142">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="52867-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52867-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-144">A intensidade de bit de cor da exibição.</span><span class="sxs-lookup"><span data-stu-id="52867-144">The color bit depth of the display.</span></span> <span data-ttu-id="52867-145">Os valores possíveis são 4, 8, 15, 16, 24 e 32.</span><span class="sxs-lookup"><span data-stu-id="52867-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="52867-146">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="52867-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-149">O conteúdo do arquivo RDP que corresponde às configurações personalizadas de RDP no Gerenciador RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="52867-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="52867-150">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="52867-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-153">O conteúdo do arquivo RDP que corresponde às configurações de implantação no Gerenciador RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="52867-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="52867-154">Se esse valor for definido, as configurações de implantação de RDP substituirão as configurações padrão nessa classe.</span><span class="sxs-lookup"><span data-stu-id="52867-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="52867-155">Por exemplo, se você definir a propriedade **GatewayAuthMode** nessa classe e definir a propriedade **DeploymentRDPSettings** , a propriedade **GatewayAuthMode** dessa classe será ignorada e o valor **GatewayAuthMode** de **DeploymentRDPSettings** será usado.</span><span class="sxs-lookup"><span data-stu-id="52867-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="52867-156">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52867-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52867-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52867-159">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="52867-159">Description of the object.</span></span>

<span data-ttu-id="52867-160">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52867-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52867-161">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="52867-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-164">O nome do servidor de Host da Sessão RD ou o FQDN (nome de domínio totalmente qualificado) do farm de servidores do Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="52867-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="52867-165">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="52867-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-166">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="52867-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52867-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-168">O método de autenticação de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="52867-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="52867-169">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="52867-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="52867-170">0</span><span class="sxs-lookup"><span data-stu-id="52867-170">0</span></span>
</dt> <dd>

<span data-ttu-id="52867-171">Senha</span><span class="sxs-lookup"><span data-stu-id="52867-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="52867-172">1</span><span class="sxs-lookup"><span data-stu-id="52867-172">1</span></span>
</dt> <dd>

<span data-ttu-id="52867-173">Cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="52867-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="52867-174">4</span><span class="sxs-lookup"><span data-stu-id="52867-174">4</span></span>
</dt> <dd>

<span data-ttu-id="52867-175">Permitir que o usuário selecione durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="52867-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52867-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="52867-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-179">O nome do servidor de gateway de área de trabalho remota a ser usado.</span><span class="sxs-lookup"><span data-stu-id="52867-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="52867-180">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="52867-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-181">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="52867-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52867-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-183">Indica se um servidor de gateway de área de trabalho remota deve ser usado para se conectar ao servidor de Host da Sessão RD de destino por um firewall.</span><span class="sxs-lookup"><span data-stu-id="52867-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="52867-184">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="52867-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="52867-185">0</span><span class="sxs-lookup"><span data-stu-id="52867-185">0</span></span>
</dt> <dd>

<span data-ttu-id="52867-186">Não use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="52867-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="52867-187">1</span><span class="sxs-lookup"><span data-stu-id="52867-187">1</span></span>
</dt> <dd>

<span data-ttu-id="52867-188">Use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="52867-188">Use an RD Gateway server.</span></span> <span data-ttu-id="52867-189">Ignore o servidor de gateway de área de trabalho remota para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="52867-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="52867-190">2</span><span class="sxs-lookup"><span data-stu-id="52867-190">2</span></span>
</dt> <dd>

<span data-ttu-id="52867-191">Use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="52867-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="52867-192">3</span><span class="sxs-lookup"><span data-stu-id="52867-192">3</span></span>
</dt> <dd>

<span data-ttu-id="52867-193">Detectar automaticamente as configurações do servidor Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="52867-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52867-194">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="52867-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-195">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52867-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52867-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-197">Quando possível, use as mesmas credenciais de usuário para o servidor de gateway de área de trabalho remota e o servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="52867-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="52867-198">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="52867-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-199">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52867-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52867-200">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-201">Indica se um certificado deve ser usado para assinar os arquivos RDP.</span><span class="sxs-lookup"><span data-stu-id="52867-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="52867-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52867-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-203">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52867-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52867-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52867-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52867-205">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="52867-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="52867-206">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="52867-206">The date the object was installed.</span></span> <span data-ttu-id="52867-207">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="52867-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="52867-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52867-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52867-209">**Nome**</span><span class="sxs-lookup"><span data-stu-id="52867-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52867-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52867-212">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="52867-212">The name of the object.</span></span>

<span data-ttu-id="52867-213">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52867-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52867-214">**Porta**</span><span class="sxs-lookup"><span data-stu-id="52867-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-215">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="52867-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52867-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-217">A porta RDP a ser usada.</span><span class="sxs-lookup"><span data-stu-id="52867-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="52867-218">**Redireçãooptions**</span><span class="sxs-lookup"><span data-stu-id="52867-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="52867-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52867-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-221">Especifica as opções de redirecionamento de dispositivo e de recurso para conexões do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="52867-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="52867-222">Os sinalizadores para **redireçãooptions** podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="52867-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="52867-223">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="52867-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="52867-224">0</span><span class="sxs-lookup"><span data-stu-id="52867-224">0</span></span>
</dt> <dd>

<span data-ttu-id="52867-225">Nenhum redirecionamento de dispositivo ou recurso.</span><span class="sxs-lookup"><span data-stu-id="52867-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="52867-226">1</span><span class="sxs-lookup"><span data-stu-id="52867-226">1</span></span>
</dt> <dd>

<span data-ttu-id="52867-227">Redirecione unidades de disco.</span><span class="sxs-lookup"><span data-stu-id="52867-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="52867-228">2</span><span class="sxs-lookup"><span data-stu-id="52867-228">2</span></span>
</dt> <dd>

<span data-ttu-id="52867-229">Redirecionar impressoras.</span><span class="sxs-lookup"><span data-stu-id="52867-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="52867-230">4</span><span class="sxs-lookup"><span data-stu-id="52867-230">4</span></span>
</dt> <dd>

<span data-ttu-id="52867-231">Redirecionar a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="52867-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="52867-232">8</span><span class="sxs-lookup"><span data-stu-id="52867-232">8</span></span>
</dt> <dd>

<span data-ttu-id="52867-233">Redirecionar dispositivos Plug and Play com suporte.</span><span class="sxs-lookup"><span data-stu-id="52867-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="52867-234">16</span><span class="sxs-lookup"><span data-stu-id="52867-234">16</span></span>
</dt> <dd>

<span data-ttu-id="52867-235">Redirecionar cartões inteligentes.</span><span class="sxs-lookup"><span data-stu-id="52867-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="52867-236">32</span><span class="sxs-lookup"><span data-stu-id="52867-236">32</span></span>
</dt> <dd>

<span data-ttu-id="52867-237">Redirecione o áudio.</span><span class="sxs-lookup"><span data-stu-id="52867-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="52867-238">64</span><span class="sxs-lookup"><span data-stu-id="52867-238">64</span></span>
</dt> <dd>

<span data-ttu-id="52867-239">Redirecione portas seriais.</span><span class="sxs-lookup"><span data-stu-id="52867-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52867-240">**RequireServerAuth**</span><span class="sxs-lookup"><span data-stu-id="52867-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-241">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52867-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52867-242">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-243">Indica se a autenticação do servidor deve ser necessária.</span><span class="sxs-lookup"><span data-stu-id="52867-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="52867-244">**Status**</span><span class="sxs-lookup"><span data-stu-id="52867-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52867-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52867-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="52867-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52867-247">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="52867-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="52867-248">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="52867-248">Current status of the object.</span></span> <span data-ttu-id="52867-249">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="52867-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="52867-250">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="52867-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="52867-251">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="52867-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="52867-252">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="52867-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="52867-253">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="52867-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="52867-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52867-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="52867-255">("OK")</span><span class="sxs-lookup"><span data-stu-id="52867-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-256">("Erro")</span><span class="sxs-lookup"><span data-stu-id="52867-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-257">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="52867-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-258">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="52867-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-259">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="52867-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-260">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="52867-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-261">("Parando")</span><span class="sxs-lookup"><span data-stu-id="52867-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="52867-262">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="52867-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52867-263">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="52867-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52867-264">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52867-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52867-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="52867-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="52867-266">Indica se vários monitores estão habilitados para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="52867-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52867-267">Comentários</span><span class="sxs-lookup"><span data-stu-id="52867-267">Remarks</span></span>

<span data-ttu-id="52867-268">Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.</span><span class="sxs-lookup"><span data-stu-id="52867-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="52867-269">Se **RequireServerAuth** for definido como **true**, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="52867-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="52867-270">Se o programa do RemoteApp for para uso na intranet e todos os computadores cliente estiverem executando o Windows Server 2008 ou o Windows Vista, você não precisará configurar o servidor de Host da Sessão RD para usar um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="52867-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="52867-271">Nesse caso, Autenticação no Nível da Rede é usado.</span><span class="sxs-lookup"><span data-stu-id="52867-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="52867-272">Você deve especificar o FQDN do servidor ou farm para o valor da propriedade **farmname** .</span><span class="sxs-lookup"><span data-stu-id="52867-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="52867-273">Para se conectar ao namespace "CIMV2 \\ TerminalServices", o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="52867-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="52867-274">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="52867-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="52867-275">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="52867-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="52867-276">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="52867-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="52867-277">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52867-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52867-278">Eles são instalados no computador quando você adiciona a função associada.</span><span class="sxs-lookup"><span data-stu-id="52867-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="52867-279">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52867-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52867-280">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52867-280">Requirements</span></span>



| <span data-ttu-id="52867-281">Requisito</span><span class="sxs-lookup"><span data-stu-id="52867-281">Requirement</span></span> | <span data-ttu-id="52867-282">Valor</span><span class="sxs-lookup"><span data-stu-id="52867-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52867-283">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52867-283">Minimum supported client</span></span><br/> | <span data-ttu-id="52867-284">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="52867-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="52867-285">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52867-285">Minimum supported server</span></span><br/> | <span data-ttu-id="52867-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52867-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52867-287">Namespace</span><span class="sxs-lookup"><span data-stu-id="52867-287">Namespace</span></span><br/>                | <span data-ttu-id="52867-288">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="52867-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="52867-289">MOF</span><span class="sxs-lookup"><span data-stu-id="52867-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52867-290"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52867-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="52867-291">DLL</span><span class="sxs-lookup"><span data-stu-id="52867-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52867-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52867-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

