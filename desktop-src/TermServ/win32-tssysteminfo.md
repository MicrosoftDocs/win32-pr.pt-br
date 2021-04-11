---
title: Classe Win32_TSSystemInfo
description: Representa o serviço de informações do servidor de publicação centralizado.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSSystemInfo Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSSystemInfo classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454972"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="a70ff-105">\_Classe Win32 TSSystemInfo</span><span class="sxs-lookup"><span data-stu-id="a70ff-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="a70ff-106">Representa o serviço de informações do servidor de publicação centralizado</span><span class="sxs-lookup"><span data-stu-id="a70ff-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="a70ff-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a70ff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70ff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a70ff-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="a70ff-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a70ff-109">Members</span></span>

<span data-ttu-id="a70ff-110">A classe **Win32 \_ TSSystemInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a70ff-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="a70ff-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a70ff-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a70ff-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a70ff-112">Properties</span></span>

<span data-ttu-id="a70ff-113">A classe **Win32 \_ TSSystemInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a70ff-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a70ff-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a70ff-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a70ff-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a70ff-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="a70ff-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a70ff-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a70ff-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a70ff-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a70ff-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-123">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a70ff-123">Description of the object.</span></span>

<span data-ttu-id="a70ff-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a70ff-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a70ff-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a70ff-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-128">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="a70ff-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-129">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a70ff-129">The date the object was installed.</span></span> <span data-ttu-id="a70ff-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="a70ff-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a70ff-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a70ff-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a70ff-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a70ff-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-135">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="a70ff-135">The name of the object.</span></span>

<span data-ttu-id="a70ff-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a70ff-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="a70ff-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a70ff-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-140">O número de versão deste provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="a70ff-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-141">**RDUGroup**</span><span class="sxs-lookup"><span data-stu-id="a70ff-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a70ff-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-144">O grupo Área de Trabalho Remota usuários, no formato SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="a70ff-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="a70ff-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="a70ff-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a70ff-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a70ff-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a70ff-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a70ff-148">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a70ff-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a70ff-149">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a70ff-149">Current status of the object.</span></span> <span data-ttu-id="a70ff-150">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a70ff-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a70ff-151">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a70ff-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a70ff-152">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a70ff-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a70ff-153">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a70ff-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a70ff-154">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a70ff-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a70ff-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a70ff-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a70ff-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="a70ff-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-157">("Erro")</span><span class="sxs-lookup"><span data-stu-id="a70ff-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-158">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="a70ff-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-159">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a70ff-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-160">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a70ff-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-161">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a70ff-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-162">("Parando")</span><span class="sxs-lookup"><span data-stu-id="a70ff-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a70ff-163">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="a70ff-163">("Service")</span></span>


<span data-ttu-id="a70ff-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a70ff-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a70ff-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a70ff-165">Requirements</span></span>



| <span data-ttu-id="a70ff-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="a70ff-166">Requirement</span></span> | <span data-ttu-id="a70ff-167">Valor</span><span class="sxs-lookup"><span data-stu-id="a70ff-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70ff-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a70ff-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a70ff-169">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a70ff-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a70ff-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a70ff-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a70ff-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a70ff-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="a70ff-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="a70ff-172">Namespace</span></span><br/>                | <span data-ttu-id="a70ff-173">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a70ff-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a70ff-174">MOF</span><span class="sxs-lookup"><span data-stu-id="a70ff-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a70ff-175"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a70ff-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="a70ff-176">DLL</span><span class="sxs-lookup"><span data-stu-id="a70ff-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a70ff-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a70ff-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

