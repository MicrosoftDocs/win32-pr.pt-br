---
title: Classe Win32_TSEnvironmentSetting
description: Define as definições de configuração para a classe de terminal do Win32, \_ incluindo a diretiva de programa inicial.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSEnvironmentSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSEnvironmentSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499720"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="20bb0-105">\_Classe Win32 TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="20bb0-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="20bb0-106">A classe WMI **\_ TSEnvironmentSetting do Win32** define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo a diretiva de programa inicial.</span><span class="sxs-lookup"><span data-stu-id="20bb0-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="20bb0-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="20bb0-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="20bb0-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="20bb0-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bb0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20bb0-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="20bb0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="20bb0-110">Members</span></span>

<span data-ttu-id="20bb0-111">A classe **Win32 \_ TSEnvironmentSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20bb0-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="20bb0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="20bb0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="20bb0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20bb0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20bb0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="20bb0-114">Methods</span></span>

<span data-ttu-id="20bb0-115">A classe **Win32 \_ TSEnvironmentSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="20bb0-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="20bb0-116">Método</span><span class="sxs-lookup"><span data-stu-id="20bb0-116">Method</span></span>                                                                      | <span data-ttu-id="20bb0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="20bb0-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="20bb0-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="20bb0-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="20bb0-119">Define as propriedades do programa de inicialização incluídas nesta classe.</span><span class="sxs-lookup"><span data-stu-id="20bb0-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="20bb0-120">**SetClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="20bb0-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="20bb0-121">Define a propriedade **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="20bb0-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="20bb0-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20bb0-122">Properties</span></span>

<span data-ttu-id="20bb0-123">A classe **Win32 \_ TSEnvironmentSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20bb0-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20bb0-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="20bb0-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20bb0-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-128">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="20bb0-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="20bb0-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="20bb0-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-133">Especifica se a imagem do papel de parede é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="20bb0-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="20bb0-134">A exibição da imagem de papel de parede pode economizar recursos do sistema diminuindo o tempo necessário para redesenhar a tela.</span><span class="sxs-lookup"><span data-stu-id="20bb0-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="20bb0-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="20bb0-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20bb0-136">A imagem do papel de parede não é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="20bb0-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="20bb0-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="20bb0-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20bb0-138">A imagem do papel de parede é exibida no cliente.</span><span class="sxs-lookup"><span data-stu-id="20bb0-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20bb0-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-142">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="20bb0-142">Description of the object.</span></span>

<span data-ttu-id="20bb0-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-144">**InitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="20bb0-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-147">O nome e o caminho do programa que o usuário executará imediatamente após o logon no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="20bb0-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-148">**InitialProgramPolicy**</span><span class="sxs-lookup"><span data-stu-id="20bb0-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20bb0-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-151">A política que o servidor usa para determinar o caminho do programa de inicialização e o nome do arquivo e o nome da pasta na qual ele está localizado.</span><span class="sxs-lookup"><span data-stu-id="20bb0-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="20bb0-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="20bb0-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20bb0-153">As configurações do programa de inicialização do usuário estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="20bb0-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="20bb0-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)</span><span class="sxs-lookup"><span data-stu-id="20bb0-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20bb0-155">As configurações do programa de inicialização do usuário são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="20bb0-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="20bb0-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Modo de aplicativo único** (2)</span><span class="sxs-lookup"><span data-stu-id="20bb0-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20bb0-157">Apenas um único aplicativo será executado nesta sessão.</span><span class="sxs-lookup"><span data-stu-id="20bb0-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="20bb0-158">As informações do programa de inicialização são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="20bb0-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20bb0-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-160">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20bb0-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-162">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="20bb0-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-163">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="20bb0-163">The date the object was installed.</span></span> <span data-ttu-id="20bb0-164">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="20bb0-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="20bb0-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20bb0-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-169">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="20bb0-169">The name of the object.</span></span>

<span data-ttu-id="20bb0-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-171">**PolicySourceClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="20bb0-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-174">Indica se a propriedade **ClientWallPaper** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="20bb0-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20bb0-175">0</span><span class="sxs-lookup"><span data-stu-id="20bb0-175">0</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-176">Servidor</span><span class="sxs-lookup"><span data-stu-id="20bb0-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-177">1</span><span class="sxs-lookup"><span data-stu-id="20bb0-177">1</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-178">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="20bb0-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-179">2</span><span class="sxs-lookup"><span data-stu-id="20bb0-179">2</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-180">Padrão</span><span class="sxs-lookup"><span data-stu-id="20bb0-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-181">**PolicySourceInitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="20bb0-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-184">Indica se a propriedade **InitialProgramPath** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="20bb0-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20bb0-185">0</span><span class="sxs-lookup"><span data-stu-id="20bb0-185">0</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-186">Servidor</span><span class="sxs-lookup"><span data-stu-id="20bb0-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-187">1</span><span class="sxs-lookup"><span data-stu-id="20bb0-187">1</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-188">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="20bb0-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-189">2</span><span class="sxs-lookup"><span data-stu-id="20bb0-189">2</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-190">Padrão</span><span class="sxs-lookup"><span data-stu-id="20bb0-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="20bb0-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-192">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-194">Indica se a propriedade de **inicialização** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="20bb0-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20bb0-195">0</span><span class="sxs-lookup"><span data-stu-id="20bb0-195">0</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-196">Servidor</span><span class="sxs-lookup"><span data-stu-id="20bb0-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-197">1</span><span class="sxs-lookup"><span data-stu-id="20bb0-197">1</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-198">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="20bb0-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-199">2</span><span class="sxs-lookup"><span data-stu-id="20bb0-199">2</span></span>
</dt> <dd>

<span data-ttu-id="20bb0-200">Padrão</span><span class="sxs-lookup"><span data-stu-id="20bb0-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="20bb0-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-204">O caminho do diretório de trabalho do programa que o usuário executará imediatamente após o logon no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="20bb0-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="20bb0-205">**Status**</span><span class="sxs-lookup"><span data-stu-id="20bb0-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-208">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="20bb0-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-209">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="20bb0-209">Current status of the object.</span></span> <span data-ttu-id="20bb0-210">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="20bb0-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="20bb0-211">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="20bb0-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="20bb0-212">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="20bb0-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="20bb0-213">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="20bb0-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="20bb0-214">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="20bb0-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="20bb0-215">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="20bb0-216">("OK")</span><span class="sxs-lookup"><span data-stu-id="20bb0-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-217">("Erro")</span><span class="sxs-lookup"><span data-stu-id="20bb0-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-218">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="20bb0-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-219">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="20bb0-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-220">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="20bb0-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-221">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="20bb0-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-222">("Parando")</span><span class="sxs-lookup"><span data-stu-id="20bb0-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20bb0-223">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="20bb0-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20bb0-224">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="20bb0-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20bb0-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20bb0-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20bb0-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20bb0-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20bb0-227">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="20bb0-227">The name of the terminal.</span></span>

<span data-ttu-id="20bb0-228">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="20bb0-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20bb0-229">Comentários</span><span class="sxs-lookup"><span data-stu-id="20bb0-229">Remarks</span></span>

<span data-ttu-id="20bb0-230">Lembre-se de que os WinStations associados à sessão de console não podem acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="20bb0-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="20bb0-231">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade **terminalname** , os métodos desse objeto retornam **WBEM \_ E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="20bb0-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="20bb0-232">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="20bb0-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="20bb0-233">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="20bb0-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="20bb0-234">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="20bb0-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="20bb0-235">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="20bb0-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="20bb0-236">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="20bb0-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="20bb0-237">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="20bb0-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20bb0-238">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="20bb0-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="20bb0-239">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="20bb0-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20bb0-240">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="20bb0-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="20bb0-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20bb0-241">Requirements</span></span>



| <span data-ttu-id="20bb0-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="20bb0-242">Requirement</span></span> | <span data-ttu-id="20bb0-243">Valor</span><span class="sxs-lookup"><span data-stu-id="20bb0-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bb0-244">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20bb0-244">Minimum supported client</span></span><br/> | <span data-ttu-id="20bb0-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20bb0-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20bb0-246">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20bb0-246">Minimum supported server</span></span><br/> | <span data-ttu-id="20bb0-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20bb0-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20bb0-248">Namespace</span><span class="sxs-lookup"><span data-stu-id="20bb0-248">Namespace</span></span><br/>                | <span data-ttu-id="20bb0-249">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="20bb0-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="20bb0-250">MOF</span><span class="sxs-lookup"><span data-stu-id="20bb0-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20bb0-251"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20bb0-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="20bb0-252">DLL</span><span class="sxs-lookup"><span data-stu-id="20bb0-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20bb0-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20bb0-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bb0-254">Confira também</span><span class="sxs-lookup"><span data-stu-id="20bb0-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bb0-255">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="20bb0-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

