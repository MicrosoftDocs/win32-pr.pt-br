---
title: Classe Win32_TSDeploymentLicensing
description: Configurações de licenciamento para a implantação de RDV (virtualização de Área de Trabalho Remota).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSDeploymentLicensing Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSDeploymentLicensing classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780566"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="f100e-105">\_Classe Win32 TSDeploymentLicensing</span><span class="sxs-lookup"><span data-stu-id="f100e-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="f100e-106">Configurações de licenciamento para a implantação de RDV (virtualização de Área de Trabalho Remota).</span><span class="sxs-lookup"><span data-stu-id="f100e-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="f100e-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f100e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f100e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f100e-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="f100e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f100e-109">Members</span></span>

<span data-ttu-id="f100e-110">A classe **Win32 \_ TSDeploymentLicensing** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f100e-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="f100e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f100e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f100e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f100e-112">Properties</span></span>

<span data-ttu-id="f100e-113">A classe **Win32 \_ TSDeploymentLicensing** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f100e-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f100e-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f100e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f100e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f100e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f100e-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f100e-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f100e-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="f100e-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f100e-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f100e-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f100e-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f100e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f100e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f100e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f100e-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="f100e-123">Description of the object.</span></span>

<span data-ttu-id="f100e-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f100e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f100e-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f100e-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f100e-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f100e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f100e-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="f100e-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f100e-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f100e-129">The date the object was installed.</span></span> <span data-ttu-id="f100e-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f100e-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f100e-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f100e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f100e-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="f100e-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f100e-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="f100e-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f100e-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f100e-135">Especifica os servidores de licença a serem usados.</span><span class="sxs-lookup"><span data-stu-id="f100e-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="f100e-136">**Licenciamento**</span><span class="sxs-lookup"><span data-stu-id="f100e-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f100e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f100e-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f100e-139">Modo de licenciamento</span><span class="sxs-lookup"><span data-stu-id="f100e-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="f100e-140">**Por dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="f100e-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="f100e-141">**Por usuário** (4)</span><span class="sxs-lookup"><span data-stu-id="f100e-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="f100e-142">**Ainda não configurado** (5)</span><span class="sxs-lookup"><span data-stu-id="f100e-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f100e-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f100e-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f100e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f100e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f100e-146">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f100e-146">The name of the object.</span></span>

<span data-ttu-id="f100e-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f100e-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f100e-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="f100e-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f100e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f100e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f100e-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f100e-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f100e-152">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f100e-152">Current status of the object.</span></span> <span data-ttu-id="f100e-153">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="f100e-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f100e-154">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="f100e-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f100e-155">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="f100e-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f100e-156">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="f100e-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f100e-157">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="f100e-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f100e-158">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f100e-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f100e-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="f100e-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-160">("Erro")</span><span class="sxs-lookup"><span data-stu-id="f100e-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-161">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="f100e-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-162">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f100e-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-163">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f100e-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-164">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f100e-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-165">("Parando")</span><span class="sxs-lookup"><span data-stu-id="f100e-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f100e-166">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="f100e-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f100e-167">**UseCentralLicensingSettings**</span><span class="sxs-lookup"><span data-stu-id="f100e-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f100e-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f100e-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f100e-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f100e-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f100e-170">Especifica se as configurações de licenciamento de toda a implantação devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="f100e-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="f100e-171">**True** para usar essas configurações para todos os servidores nesta implantação.</span><span class="sxs-lookup"><span data-stu-id="f100e-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="f100e-172">**false** para defini-los por servidor.</span><span class="sxs-lookup"><span data-stu-id="f100e-172">**false** to set them per-server.</span></span> <span data-ttu-id="f100e-173">Se isso for definido como **false**, todas as outras configurações de licenciamento serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="f100e-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f100e-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f100e-174">Requirements</span></span>



| <span data-ttu-id="f100e-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="f100e-175">Requirement</span></span> | <span data-ttu-id="f100e-176">Valor</span><span class="sxs-lookup"><span data-stu-id="f100e-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f100e-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f100e-177">Minimum supported client</span></span><br/> | <span data-ttu-id="f100e-178">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f100e-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f100e-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f100e-179">Minimum supported server</span></span><br/> | <span data-ttu-id="f100e-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f100e-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="f100e-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="f100e-181">Namespace</span></span><br/>                | <span data-ttu-id="f100e-182">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f100e-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f100e-183">MOF</span><span class="sxs-lookup"><span data-stu-id="f100e-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f100e-184"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f100e-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f100e-185">DLL</span><span class="sxs-lookup"><span data-stu-id="f100e-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f100e-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f100e-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

