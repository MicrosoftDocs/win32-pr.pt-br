---
description: A classe de compartilhamento do Win32 \_ representa um recurso compartilhado em um sistema de computador executando o Windows. Isso pode ser uma unidade de disco, uma impressora, uma comunicação entre processos ou outro dispositivo compartilhável. Para obter mais informações sobre como recuperar classes WMI, consulte Recuperando uma classe.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089456"
---
# <a name="win32_share-class"></a><span data-ttu-id="d0868-105">\_Classe de compartilhamento Win32</span><span class="sxs-lookup"><span data-stu-id="d0868-105">Win32\_Share class</span></span>

<span data-ttu-id="d0868-106">A classe de **\_ compartilhamento do Win32** representa um recurso compartilhado em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="d0868-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="d0868-107">Isso pode ser uma unidade de disco, uma impressora, uma comunicação entre processos ou outro dispositivo compartilhável.</span><span class="sxs-lookup"><span data-stu-id="d0868-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="d0868-108">Para obter mais informações sobre como recuperar classes WMI, consulte [recuperando uma classe](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="d0868-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d0868-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d0868-110">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="d0868-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0868-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0868-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="d0868-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d0868-112">Members</span></span>

<span data-ttu-id="d0868-113">A classe de **\_ compartilhamento do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d0868-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="d0868-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0868-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0868-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0868-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0868-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0868-116">Methods</span></span>

<span data-ttu-id="d0868-117">A classe de **\_ compartilhamento do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d0868-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="d0868-118">Método</span><span class="sxs-lookup"><span data-stu-id="d0868-118">Method</span></span>                                                             | <span data-ttu-id="d0868-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0868-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0868-120">**Criada**</span><span class="sxs-lookup"><span data-stu-id="d0868-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="d0868-121">Método de classe que inicia o compartilhamento para um recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="d0868-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="d0868-122">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="d0868-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="d0868-123">Método de classe que exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor, desconectando as conexões com o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d0868-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="d0868-124">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="d0868-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="d0868-125">Retorna os direitos de acesso ao compartilhamento mantido pelo usuário ou grupo em cujo nome a instância é retornada.</span><span class="sxs-lookup"><span data-stu-id="d0868-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="d0868-126">Você deve usar esse método no lugar da propriedade **AccessMask** , que é sempre **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d0868-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="d0868-127">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="d0868-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="d0868-128">Método de classe que define os parâmetros de um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d0868-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="d0868-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0868-129">Properties</span></span>

<span data-ttu-id="d0868-130">A classe de **\_ compartilhamento do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d0868-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0868-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="d0868-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0868-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-134">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d0868-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d0868-135">Esta propriedade é obsoleta e não é mais usada.</span><span class="sxs-lookup"><span data-stu-id="d0868-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="d0868-136">Em vez disso, use o método [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="d0868-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="d0868-137">O valor da propriedade **AccessMask** é definido como **NULL** pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="d0868-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="d0868-138">Para obter mais informações sobre como definir o acesso quando um compartilhamento é criado, consulte o método [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="d0868-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d0868-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="d0868-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d0868-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-142">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="d0868-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-143">O número de usuários simultâneos deste recurso foi limitado.</span><span class="sxs-lookup"><span data-stu-id="d0868-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="d0868-144">Se **for true**, o valor na propriedade **MaximumAllowed** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="d0868-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d0868-145">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d0868-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0868-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-148">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d0868-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-149">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d0868-149">A short textual description of the object.</span></span>

<span data-ttu-id="d0868-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0868-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d0868-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0868-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-154">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="d0868-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-155">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d0868-155">A textual description of the object.</span></span>

<span data-ttu-id="d0868-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0868-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0868-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-158">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0868-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-160">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="d0868-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-161">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d0868-161">Indicates when the object was installed.</span></span> <span data-ttu-id="d0868-162">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d0868-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d0868-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0868-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="d0868-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0868-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-167">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("as \| estruturas de gerenciamento de rede do Win32API \| [**compartilham \_ informações \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")</span><span class="sxs-lookup"><span data-stu-id="d0868-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-168">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="d0868-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="d0868-169">O valor só será válido se a propriedade **AllowMaximum** estiver definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="d0868-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d0868-170">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d0868-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0868-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-173">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| [**share \_ info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="d0868-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-174">Alias fornecido a um caminho configurado como um compartilhamento em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="d0868-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="d0868-175">Windows 2008 exemplo: " \\ Server01 \\ Public"-o windows Server 2008 requer que você coloque o UNC no nome.</span><span class="sxs-lookup"><span data-stu-id="d0868-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="d0868-176">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="d0868-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0868-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-179">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estruturas de gerenciamento de rede do win32api \| \| [**compartilham \_ informações \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ caminho")</span><span class="sxs-lookup"><span data-stu-id="d0868-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-180">Caminho local do compartilhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="d0868-180">Local path of the Windows share.</span></span>

<span data-ttu-id="d0868-181">Exemplo: "C: \\ arquivos de programas"</span><span class="sxs-lookup"><span data-stu-id="d0868-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="d0868-182">**Status**</span><span class="sxs-lookup"><span data-stu-id="d0868-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0868-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-185">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="d0868-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-186">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d0868-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="d0868-187">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="d0868-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d0868-188">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="d0868-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d0868-189">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="d0868-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d0868-190">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d0868-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d0868-191">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d0868-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d0868-192">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d0868-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d0868-193">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0868-194">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d0868-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0868-195">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d0868-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0868-196">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="d0868-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0868-197">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d0868-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0868-198">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d0868-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0868-199">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d0868-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0868-200">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d0868-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0868-201">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="d0868-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0868-202">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="d0868-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0868-203">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="d0868-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0868-204">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d0868-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0868-205">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="d0868-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0868-206">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="d0868-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0868-207">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d0868-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0868-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0868-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0868-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0868-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0868-210">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api informações de \| [**compartilhamento \_ \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ tipo")</span><span class="sxs-lookup"><span data-stu-id="d0868-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="d0868-211">Tipo de recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d0868-211">Type of resource being shared.</span></span> <span data-ttu-id="d0868-212">Os tipos incluem: unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.</span><span class="sxs-lookup"><span data-stu-id="d0868-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="d0868-213">**Unidade de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="d0868-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="d0868-214">**Fila de impressão** (1)</span><span class="sxs-lookup"><span data-stu-id="d0868-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="d0868-215">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="d0868-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="d0868-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="d0868-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="d0868-217">**Administrador da unidade de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="d0868-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="d0868-218">**Administrador da fila de impressão** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="d0868-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="d0868-219">**Administrador do dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="d0868-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="d0868-220">**Administrador de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="d0868-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="d0868-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0868-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d0868-222">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0868-222">Remarks</span></span>

<span data-ttu-id="d0868-223">A classe de **\_ compartilhamento do Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0868-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="d0868-224">O método Create nessa classe é um método estático.</span><span class="sxs-lookup"><span data-stu-id="d0868-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="d0868-225">Os métodos **delete**, **GetAccessMask** e **SetShareInfo** são todos métodos de instância.</span><span class="sxs-lookup"><span data-stu-id="d0868-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="d0868-226">Dependendo de suas permissões de segurança, talvez você não consiga recuperar todas as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d0868-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="d0868-227">Por exemplo, as propriedades **AllowMaximum**, **MaximumAllowed**, **Path** e **Type** podem retornar NULL.</span><span class="sxs-lookup"><span data-stu-id="d0868-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="d0868-228">Em geral, os usuários avançados e os administradores poderão recuperar todos os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0868-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="d0868-229">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0868-229">Examples</span></span>

<span data-ttu-id="d0868-230">O[exemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) do script Center a seguir lista todos os compartilhamentos em um computador e lista todas as permissões de compartilhamento para cada compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d0868-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="d0868-231">O exemplo [Get share Information semelhantes to Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample consulta \_ o Win32 share e fornece os resultados.</span><span class="sxs-lookup"><span data-stu-id="d0868-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="d0868-232">O exemplo do PowerShell a seguir exibe os compartilhamentos no sistema local.</span><span class="sxs-lookup"><span data-stu-id="d0868-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="d0868-233">Como alternativa, se você quiser filtrar com mais precisão, poderá usar o seguinte trecho do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d0868-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="d0868-234">O exemplo de VBScript a seguir exibe os compartilhamentos no sistema local.</span><span class="sxs-lookup"><span data-stu-id="d0868-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="d0868-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0868-235">Requirements</span></span>



| <span data-ttu-id="d0868-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0868-236">Requirement</span></span> | <span data-ttu-id="d0868-237">Valor</span><span class="sxs-lookup"><span data-stu-id="d0868-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0868-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0868-238">Minimum supported client</span></span><br/> | <span data-ttu-id="d0868-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0868-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0868-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0868-240">Minimum supported server</span></span><br/> | <span data-ttu-id="d0868-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0868-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0868-242">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0868-242">Namespace</span></span><br/>                | <span data-ttu-id="d0868-243">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d0868-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0868-244">MOF</span><span class="sxs-lookup"><span data-stu-id="d0868-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0868-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0868-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0868-246">DLL</span><span class="sxs-lookup"><span data-stu-id="d0868-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0868-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0868-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0868-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0868-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0868-249">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d0868-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d0868-250">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d0868-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d0868-251">Tarefas do WMI: arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="d0868-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
