---
description: A \_ classe Win32 ClusterShare representa um recurso compartilhado em um cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089473"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="07383-103">\_Classe Win32 ClusterShare</span><span class="sxs-lookup"><span data-stu-id="07383-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="07383-104">\[A classe **Win32 \_ ClusterShare** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="07383-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="07383-105">Em vez disso, use as classes de [**\_ compartilhamento MSFT**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) e [**MSFT \_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) .\]</span><span class="sxs-lookup"><span data-stu-id="07383-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="07383-106">A \_ classe Win32 ClusterShare representa um recurso compartilhado em um cluster.</span><span class="sxs-lookup"><span data-stu-id="07383-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="07383-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="07383-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07383-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07383-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="07383-109">Membros</span><span class="sxs-lookup"><span data-stu-id="07383-109">Members</span></span>

<span data-ttu-id="07383-110">A classe **Win32 \_ ClusterShare** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="07383-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="07383-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="07383-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="07383-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07383-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07383-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="07383-113">Methods</span></span>

<span data-ttu-id="07383-114">A classe **Win32 \_ ClusterShare** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="07383-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="07383-115">Método</span><span class="sxs-lookup"><span data-stu-id="07383-115">Method</span></span>                                                    | <span data-ttu-id="07383-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="07383-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="07383-117">**Criada**</span><span class="sxs-lookup"><span data-stu-id="07383-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="07383-118">Cria uma nova instância de **\_ ClusterShare do Win32** .</span><span class="sxs-lookup"><span data-stu-id="07383-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="07383-119">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="07383-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="07383-120">Exclui uma instância de **\_ ClusterShare do Win32** .</span><span class="sxs-lookup"><span data-stu-id="07383-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="07383-121">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="07383-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="07383-122">Retorna um bitmap com os direitos de acesso ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="07383-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="07383-123">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="07383-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="07383-124">Define os parâmetros do recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="07383-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="07383-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07383-125">Properties</span></span>

<span data-ttu-id="07383-126">A classe **Win32 \_ ClusterShare** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="07383-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07383-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="07383-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07383-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07383-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-130">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07383-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07383-131">Esta propriedade é obsoleta e não é mais usada.</span><span class="sxs-lookup"><span data-stu-id="07383-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="07383-132">Em vez disso, use o método [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="07383-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="07383-133">O valor da propriedade **AccessMask** é definido como **NULL** pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="07383-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="07383-134">Para obter mais informações sobre como definir o acesso quando um compartilhamento é criado, consulte o método [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="07383-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="07383-135">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="07383-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="07383-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07383-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="07383-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="07383-140">O número de usuários simultâneos deste recurso foi limitado.</span><span class="sxs-lookup"><span data-stu-id="07383-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="07383-141">Se **for true**, o valor na propriedade **MaximumAllowed** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="07383-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="07383-142">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-143">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="07383-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="07383-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07383-147">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="07383-147">A short textual description of the object.</span></span>

<span data-ttu-id="07383-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07383-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-149">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="07383-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-152">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="07383-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07383-153">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="07383-153">A textual description of the object.</span></span>

<span data-ttu-id="07383-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07383-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07383-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-156">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07383-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07383-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-158">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="07383-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07383-159">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="07383-159">Indicates when the object was installed.</span></span> <span data-ttu-id="07383-160">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="07383-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="07383-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07383-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="07383-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07383-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07383-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-165">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="07383-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="07383-166">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="07383-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="07383-167">O valor só será válido se a propriedade **AllowMaximum** estiver definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="07383-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="07383-168">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="07383-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-172">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| estruturas de gerenciamento de rede \| [**compartilham \_ informações \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="07383-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="07383-173">Alias fornecido a um caminho configurado como um compartilhamento em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="07383-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="07383-174">Windows 2008 exemplo: " \\ Server01 \\ Public"-o windows Server 2008 requer que você coloque o UNC no nome.</span><span class="sxs-lookup"><span data-stu-id="07383-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="07383-175">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-176">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="07383-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-179">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("estruturas de gerenciamento de rede do win32api \| \| [**compartilham \_ informações \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ caminho")</span><span class="sxs-lookup"><span data-stu-id="07383-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="07383-180">Caminho local do compartilhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="07383-180">Local path of the Windows share.</span></span>

<span data-ttu-id="07383-181">Exemplo: "C: \\ arquivos de programas"</span><span class="sxs-lookup"><span data-stu-id="07383-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="07383-182">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="07383-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="07383-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-186">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("servername"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management estruturas \| [**share \_ info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")</span><span class="sxs-lookup"><span data-stu-id="07383-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="07383-187">O servidor de cluster no qual o compartilhamento está hospedado.</span><span class="sxs-lookup"><span data-stu-id="07383-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="07383-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="07383-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07383-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07383-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-191">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="07383-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07383-192">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="07383-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="07383-193">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="07383-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="07383-194">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="07383-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="07383-195">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="07383-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="07383-196">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="07383-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07383-197">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="07383-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07383-198">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="07383-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07383-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07383-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07383-200">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="07383-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07383-201">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="07383-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07383-202">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="07383-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07383-203">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="07383-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07383-204">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="07383-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07383-205">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="07383-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07383-206">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="07383-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07383-207">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="07383-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07383-208">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="07383-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07383-209">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="07383-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07383-210">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="07383-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07383-211">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="07383-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07383-212">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="07383-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07383-213">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="07383-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07383-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07383-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07383-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07383-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07383-216">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de gerenciamento de rede win32api informações de \| [**compartilhamento \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ tipo")</span><span class="sxs-lookup"><span data-stu-id="07383-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="07383-217">Tipo de recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="07383-217">Type of resource being shared.</span></span> <span data-ttu-id="07383-218">Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.</span><span class="sxs-lookup"><span data-stu-id="07383-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="07383-219">Essa propriedade é herdada [**do \_ compartilhamento do Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="07383-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="07383-220">**Unidade de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="07383-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="07383-221">**Fila de impressão** (1)</span><span class="sxs-lookup"><span data-stu-id="07383-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="07383-222">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="07383-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="07383-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="07383-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="07383-224">**Administrador da unidade de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="07383-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="07383-225">**Administrador da fila de impressão** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="07383-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="07383-226">**Administrador do dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="07383-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="07383-227">**Administrador de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="07383-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="07383-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="07383-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="07383-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07383-229">Requirements</span></span>



| <span data-ttu-id="07383-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="07383-230">Requirement</span></span> | <span data-ttu-id="07383-231">Valor</span><span class="sxs-lookup"><span data-stu-id="07383-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07383-232">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07383-232">Minimum supported client</span></span><br/> | <span data-ttu-id="07383-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07383-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="07383-234">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07383-234">Minimum supported server</span></span><br/> | <span data-ttu-id="07383-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07383-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="07383-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="07383-236">Namespace</span></span><br/>                | <span data-ttu-id="07383-237">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="07383-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07383-238">MOF</span><span class="sxs-lookup"><span data-stu-id="07383-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07383-239"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07383-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07383-240">DLL</span><span class="sxs-lookup"><span data-stu-id="07383-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07383-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07383-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07383-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="07383-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07383-243">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="07383-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

