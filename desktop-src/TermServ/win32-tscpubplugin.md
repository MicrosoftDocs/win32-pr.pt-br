---
title: Classe Win32_TSCPubPlugin
description: Representa um plug-in configurado para ser usado por meio do serviço de Gerenciamento de Conexão de RemoteApp e Área de Trabalho.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSCPubPlugin Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSCPubPlugin classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824354"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="62c01-105">\_Classe Win32 TSCPubPlugin</span><span class="sxs-lookup"><span data-stu-id="62c01-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="62c01-106">Representa um plug-in configurado para ser usado por meio do serviço de Gerenciamento de Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c01-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="62c01-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="62c01-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c01-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62c01-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="62c01-109">Membros</span><span class="sxs-lookup"><span data-stu-id="62c01-109">Members</span></span>

<span data-ttu-id="62c01-110">A classe **Win32 \_ TSCPubPlugin** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62c01-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="62c01-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62c01-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62c01-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62c01-112">Properties</span></span>

<span data-ttu-id="62c01-113">A classe **Win32 \_ TSCPubPlugin** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62c01-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62c01-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="62c01-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62c01-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c01-117">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="62c01-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62c01-118">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="62c01-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="62c01-119">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62c01-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62c01-120">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="62c01-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62c01-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c01-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62c01-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62c01-124">O CLSID do plug-in.</span><span class="sxs-lookup"><span data-stu-id="62c01-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="62c01-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62c01-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62c01-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62c01-128">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="62c01-128">Description of the object.</span></span>

<span data-ttu-id="62c01-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62c01-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62c01-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62c01-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-131">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62c01-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c01-133">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="62c01-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="62c01-134">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="62c01-134">The date the object was installed.</span></span> <span data-ttu-id="62c01-135">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="62c01-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="62c01-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62c01-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62c01-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="62c01-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62c01-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62c01-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62c01-140">Especifica se o plug-in está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62c01-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="62c01-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="62c01-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62c01-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62c01-144">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="62c01-144">The name of the object.</span></span>

<span data-ttu-id="62c01-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62c01-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62c01-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="62c01-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c01-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62c01-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c01-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62c01-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c01-149">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="62c01-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="62c01-150">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="62c01-150">Current status of the object.</span></span> <span data-ttu-id="62c01-151">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="62c01-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="62c01-152">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="62c01-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="62c01-153">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="62c01-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="62c01-154">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="62c01-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="62c01-155">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="62c01-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="62c01-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62c01-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="62c01-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="62c01-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-158">("Erro")</span><span class="sxs-lookup"><span data-stu-id="62c01-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="62c01-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-160">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="62c01-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="62c01-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="62c01-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-163">("Parando")</span><span class="sxs-lookup"><span data-stu-id="62c01-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62c01-164">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="62c01-164">("Service")</span></span>


<span data-ttu-id="62c01-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62c01-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="62c01-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c01-166">Requirements</span></span>



| <span data-ttu-id="62c01-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c01-167">Requirement</span></span> | <span data-ttu-id="62c01-168">Valor</span><span class="sxs-lookup"><span data-stu-id="62c01-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c01-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c01-169">Minimum supported client</span></span><br/> | <span data-ttu-id="62c01-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62c01-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="62c01-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c01-171">Minimum supported server</span></span><br/> | <span data-ttu-id="62c01-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62c01-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="62c01-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="62c01-173">Namespace</span></span><br/>                | <span data-ttu-id="62c01-174">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="62c01-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="62c01-175">MOF</span><span class="sxs-lookup"><span data-stu-id="62c01-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c01-176"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62c01-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="62c01-177">DLL</span><span class="sxs-lookup"><span data-stu-id="62c01-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c01-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c01-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

