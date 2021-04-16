---
title: Classe Win32_TSApplicationFileExtensions
description: As extensões de nome de arquivo que são manipuladas por um aplicativo em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSApplicationFileExtensions Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSApplicationFileExtensions classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779266"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="75d6a-105">\_Classe Win32 TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="75d6a-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="75d6a-106">Descreve as extensões de nome de arquivo que são manipuladas por um aplicativo em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="75d6a-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75d6a-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="75d6a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="75d6a-108">Members</span></span>

<span data-ttu-id="75d6a-109">A classe **Win32 \_ TSApplicationFileExtensions** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75d6a-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="75d6a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="75d6a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="75d6a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75d6a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="75d6a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="75d6a-112">Methods</span></span>

<span data-ttu-id="75d6a-113">A classe **Win32 \_ TSApplicationFileExtensions** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="75d6a-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="75d6a-114">Método</span><span class="sxs-lookup"><span data-stu-id="75d6a-114">Method</span></span>                                                                         | <span data-ttu-id="75d6a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="75d6a-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75d6a-116">**Associações de**</span><span class="sxs-lookup"><span data-stu-id="75d6a-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="75d6a-117">Examina o registro para obter as associações de arquivo atuais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d6a-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="75d6a-118">**FileExtensions**</span><span class="sxs-lookup"><span data-stu-id="75d6a-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="75d6a-119">Fornece uma lista das extensões de nome de arquivo que são manipuladas por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d6a-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="75d6a-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75d6a-120">Properties</span></span>

<span data-ttu-id="75d6a-121">A classe **Win32 \_ TSApplicationFileExtensions** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="75d6a-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75d6a-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="75d6a-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d6a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75d6a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75d6a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-125">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="75d6a-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="75d6a-126">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="75d6a-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="75d6a-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75d6a-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d6a-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75d6a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d6a-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75d6a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75d6a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75d6a-131">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="75d6a-131">Description of the object.</span></span>

<span data-ttu-id="75d6a-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75d6a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d6a-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="75d6a-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d6a-134">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="75d6a-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75d6a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-136">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="75d6a-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="75d6a-137">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="75d6a-137">The date the object was installed.</span></span> <span data-ttu-id="75d6a-138">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="75d6a-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="75d6a-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75d6a-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d6a-140">**Nome**</span><span class="sxs-lookup"><span data-stu-id="75d6a-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d6a-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75d6a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75d6a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75d6a-143">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="75d6a-143">The name of the object.</span></span>

<span data-ttu-id="75d6a-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75d6a-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="75d6a-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="75d6a-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d6a-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75d6a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75d6a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75d6a-148">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="75d6a-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="75d6a-149">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="75d6a-149">Current status of the object.</span></span> <span data-ttu-id="75d6a-150">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="75d6a-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="75d6a-151">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="75d6a-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="75d6a-152">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="75d6a-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="75d6a-153">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="75d6a-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="75d6a-154">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="75d6a-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="75d6a-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="75d6a-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="75d6a-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="75d6a-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-157">("Erro")</span><span class="sxs-lookup"><span data-stu-id="75d6a-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-158">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="75d6a-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-159">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="75d6a-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-160">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="75d6a-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-161">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="75d6a-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-162">("Parando")</span><span class="sxs-lookup"><span data-stu-id="75d6a-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="75d6a-163">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="75d6a-163">("Service")</span></span>


<span data-ttu-id="75d6a-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="75d6a-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="75d6a-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="75d6a-165">Remarks</span></span>

<span data-ttu-id="75d6a-166">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="75d6a-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="75d6a-167">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="75d6a-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="75d6a-168">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="75d6a-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="75d6a-169">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="75d6a-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="75d6a-170">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="75d6a-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="75d6a-171">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75d6a-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="75d6a-172">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="75d6a-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="75d6a-173">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="75d6a-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="75d6a-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75d6a-174">Requirements</span></span>



| <span data-ttu-id="75d6a-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d6a-175">Requirement</span></span> | <span data-ttu-id="75d6a-176">Valor</span><span class="sxs-lookup"><span data-stu-id="75d6a-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d6a-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75d6a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="75d6a-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75d6a-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75d6a-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75d6a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="75d6a-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75d6a-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75d6a-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="75d6a-181">Namespace</span></span><br/>                | <span data-ttu-id="75d6a-182">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="75d6a-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="75d6a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="75d6a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75d6a-184"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75d6a-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="75d6a-185">DLL</span><span class="sxs-lookup"><span data-stu-id="75d6a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d6a-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d6a-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

