---
title: Classe Win32_RDMSVirtualDesktopCollection
description: Cria e gerencia uma coleção de áreas de trabalho virtuais.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSVirtualDesktopCollection classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780567"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="b5377-105">\_Classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="b5377-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="b5377-106">Cria e gerencia uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="b5377-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b5377-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5377-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5377-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="b5377-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b5377-109">Members</span></span>

<span data-ttu-id="b5377-110">A classe **Win32 \_ RDMSVirtualDesktopCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b5377-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="b5377-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5377-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b5377-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5377-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b5377-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5377-113">Methods</span></span>

<span data-ttu-id="b5377-114">A classe **Win32 \_ RDMSVirtualDesktopCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b5377-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="b5377-115">Método</span><span class="sxs-lookup"><span data-stu-id="b5377-115">Method</span></span>                                                                                            | <span data-ttu-id="b5377-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5377-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5377-117">**AddVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="b5377-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="b5377-118">Adiciona uma área de trabalho virtual a uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="b5377-119">**CancelPatch**</span><span class="sxs-lookup"><span data-stu-id="b5377-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="b5377-120">Cancela um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="b5377-121">**Getint32property**</span><span class="sxs-lookup"><span data-stu-id="b5377-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="b5377-122">Recupera um valor de propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="b5377-123">**Getpatchproperties**</span><span class="sxs-lookup"><span data-stu-id="b5377-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="b5377-124">Recupera as propriedades de um trabalho de provisionamento de atualização de software para as máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="b5377-125">**Getstringproperty**</span><span class="sxs-lookup"><span data-stu-id="b5377-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="b5377-126">Recupera um valor de propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="b5377-127">**ProvisioningEnumerateJobs**</span><span class="sxs-lookup"><span data-stu-id="b5377-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="b5377-128">Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.</span><span class="sxs-lookup"><span data-stu-id="b5377-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="b5377-129">**ProvisioningJobCancel**</span><span class="sxs-lookup"><span data-stu-id="b5377-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="b5377-130">Cancela um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5377-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="b5377-131">**ProvisioningJobExecute**</span><span class="sxs-lookup"><span data-stu-id="b5377-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="b5377-132">Executa um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5377-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="b5377-133">**ProvisioningJobGetReport**</span><span class="sxs-lookup"><span data-stu-id="b5377-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="b5377-134">Obtém um relatório sobre o status de um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5377-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="b5377-135">**ProvisioningPrepJob**</span><span class="sxs-lookup"><span data-stu-id="b5377-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="b5377-136">Cria um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5377-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="b5377-137">**RemoveVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="b5377-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="b5377-138">Remove uma área de trabalho virtual de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="b5377-139">**SchedulePatch**</span><span class="sxs-lookup"><span data-stu-id="b5377-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="b5377-140">Agenda um trabalho de provisionamento de atualização de software que instala atualizações de software nas máquinas virtuais em uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="b5377-141">**Setint32property**</span><span class="sxs-lookup"><span data-stu-id="b5377-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="b5377-142">Atualiza um valor de propriedade de inteiro de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="b5377-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="b5377-143">**Setstringproperty**</span><span class="sxs-lookup"><span data-stu-id="b5377-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="b5377-144">Atualiza um valor de propriedade de cadeia de caracteres de uma coleção de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="b5377-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="b5377-145">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5377-145">Properties</span></span>

<span data-ttu-id="b5377-146">A classe **Win32 \_ RDMSVirtualDesktopCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5377-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5377-147">**Alias**</span><span class="sxs-lookup"><span data-stu-id="b5377-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-150">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5377-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-151">Obtém ou define o alias da coleção</span><span class="sxs-lookup"><span data-stu-id="b5377-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="b5377-152">**CollectionDescription**</span><span class="sxs-lookup"><span data-stu-id="b5377-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-155">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5377-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-156">Obtém ou define a descrição da coleção</span><span class="sxs-lookup"><span data-stu-id="b5377-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="b5377-157">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="b5377-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-158">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="b5377-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b5377-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-160">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5377-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-161">Obtém ou define uma matriz de valores que especificam ícones para a coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-162">**IsHA**</span><span class="sxs-lookup"><span data-stu-id="b5377-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-163">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5377-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-165">Obtém ou define um valor que indica se a coleção contém VMs altamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b5377-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="b5377-166">**True** se a coleção contiver VMs altamente disponíveis; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5377-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="b5377-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5377-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-170">Obtém ou define um valor que indica se a coleção é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b5377-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="b5377-171">**True** se a coleção for gerenciada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5377-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-172">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="b5377-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-173">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5377-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-175">Obtém ou define um valor que indica se um usuário é um administrador em uma VM.</span><span class="sxs-lookup"><span data-stu-id="b5377-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="b5377-176">**True** se o usuário for um administrador em uma VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5377-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b5377-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-180">Obtém ou define o nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-181">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="b5377-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-182">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5377-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-184">Obtém ou define um valor que indica se uma VM foi revertida com um instantâneo de VM.</span><span class="sxs-lookup"><span data-stu-id="b5377-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="b5377-185">**True** se a VM foi revertida com um instantâneo de VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5377-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b5377-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-189">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5377-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-190">Obtém ou define um descritor de segurança com formato SSDL que controla o acesso à coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-191">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="b5377-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-192">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5377-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-194">Obtém ou define um valor que indica se a coleção é exibida no Terminal Services Acesso via Web (TS Acesso via Web).</span><span class="sxs-lookup"><span data-stu-id="b5377-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="b5377-195">**True** para exibir a coleção no TS acesso via Web; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b5377-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-196">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5377-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5377-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b5377-199">Obtém ou define um valor que indica o tipo de sessões de máquina virtual hospedadas pela coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="b5377-200">Essa propriedade contém um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b5377-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="b5377-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="b5377-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b5377-202">Máquinas virtuais temporárias.</span><span class="sxs-lookup"><span data-stu-id="b5377-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="b5377-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="b5377-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b5377-204">Máquinas virtuais criadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="b5377-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="b5377-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="b5377-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b5377-206">Máquinas virtuais geradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b5377-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b5377-207">**UserVHDSetting**</span><span class="sxs-lookup"><span data-stu-id="b5377-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-209">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-210">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5377-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-211">Obtém ou define a configuração de VHD de dados de usuário para a coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="b5377-212">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="b5377-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5377-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5377-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5377-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b5377-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b5377-215">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5377-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5377-216">Obtém ou define as configurações da área de trabalho das máquinas virtuais na coleção.</span><span class="sxs-lookup"><span data-stu-id="b5377-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5377-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5377-217">Requirements</span></span>



| <span data-ttu-id="b5377-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5377-218">Requirement</span></span> | <span data-ttu-id="b5377-219">Valor</span><span class="sxs-lookup"><span data-stu-id="b5377-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5377-220">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5377-220">Minimum supported client</span></span><br/> | <span data-ttu-id="b5377-221">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b5377-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b5377-222">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5377-222">Minimum supported server</span></span><br/> | <span data-ttu-id="b5377-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b5377-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b5377-224">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5377-224">Namespace</span></span><br/>                | <span data-ttu-id="b5377-225">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="b5377-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b5377-226">MOF</span><span class="sxs-lookup"><span data-stu-id="b5377-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5377-227"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5377-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5377-228">DLL</span><span class="sxs-lookup"><span data-stu-id="b5377-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5377-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5377-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b5377-230">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5377-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5377-231">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b5377-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

