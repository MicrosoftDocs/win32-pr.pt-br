---
title: Classe Win32_TSExpandEnvironmentVariables
description: Expande variáveis de ambiente definidas pelo sistema. | Classe Win32_TSExpandEnvironmentVariables
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSExpandEnvironmentVariables Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSExpandEnvironmentVariables classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837833"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="d69bf-106">\_Classe Win32 TSExpandEnvironmentVariables</span><span class="sxs-lookup"><span data-stu-id="d69bf-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="d69bf-107">Expande variáveis de ambiente definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d69bf-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69bf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d69bf-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d69bf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d69bf-109">Members</span></span>

<span data-ttu-id="d69bf-110">A classe **Win32 \_ TSExpandEnvironmentVariables** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d69bf-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="d69bf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d69bf-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d69bf-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d69bf-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d69bf-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d69bf-113">Methods</span></span>

<span data-ttu-id="d69bf-114">A classe **Win32 \_ TSExpandEnvironmentVariables** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d69bf-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="d69bf-115">Método</span><span class="sxs-lookup"><span data-stu-id="d69bf-115">Method</span></span>                                                                                  | <span data-ttu-id="d69bf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d69bf-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="d69bf-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="d69bf-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="d69bf-118">Expande variáveis de ambiente definidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d69bf-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d69bf-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d69bf-119">Properties</span></span>

<span data-ttu-id="d69bf-120">A classe **Win32 \_ TSExpandEnvironmentVariables** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d69bf-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d69bf-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d69bf-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69bf-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d69bf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d69bf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d69bf-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d69bf-125">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="d69bf-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d69bf-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d69bf-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d69bf-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d69bf-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69bf-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d69bf-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d69bf-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d69bf-130">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d69bf-130">Description of the object.</span></span>

<span data-ttu-id="d69bf-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d69bf-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d69bf-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d69bf-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69bf-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d69bf-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d69bf-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-135">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="d69bf-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d69bf-136">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d69bf-136">The date the object was installed.</span></span> <span data-ttu-id="d69bf-137">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d69bf-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d69bf-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d69bf-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d69bf-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d69bf-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69bf-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d69bf-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d69bf-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d69bf-142">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="d69bf-142">The name of the object.</span></span>

<span data-ttu-id="d69bf-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d69bf-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d69bf-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="d69bf-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d69bf-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d69bf-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d69bf-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d69bf-147">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d69bf-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d69bf-148">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d69bf-148">Current status of the object.</span></span> <span data-ttu-id="d69bf-149">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d69bf-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d69bf-150">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d69bf-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d69bf-151">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d69bf-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d69bf-152">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d69bf-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d69bf-153">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d69bf-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d69bf-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d69bf-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d69bf-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="d69bf-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-156">("Erro")</span><span class="sxs-lookup"><span data-stu-id="d69bf-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-157">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d69bf-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-158">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d69bf-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-159">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d69bf-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-160">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d69bf-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-161">("Parando")</span><span class="sxs-lookup"><span data-stu-id="d69bf-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d69bf-162">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="d69bf-162">("Service")</span></span>


<span data-ttu-id="d69bf-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d69bf-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d69bf-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="d69bf-164">Remarks</span></span>

<span data-ttu-id="d69bf-165">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="d69bf-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d69bf-166">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="d69bf-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="d69bf-167">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="d69bf-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d69bf-168">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="d69bf-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d69bf-169">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d69bf-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d69bf-170">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d69bf-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d69bf-171">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d69bf-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d69bf-172">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d69bf-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d69bf-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d69bf-173">Requirements</span></span>



| <span data-ttu-id="d69bf-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69bf-174">Requirement</span></span> | <span data-ttu-id="d69bf-175">Valor</span><span class="sxs-lookup"><span data-stu-id="d69bf-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d69bf-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d69bf-176">Minimum supported client</span></span><br/> | <span data-ttu-id="d69bf-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d69bf-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d69bf-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d69bf-178">Minimum supported server</span></span><br/> | <span data-ttu-id="d69bf-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d69bf-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d69bf-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="d69bf-180">Namespace</span></span><br/>                | <span data-ttu-id="d69bf-181">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d69bf-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d69bf-182">MOF</span><span class="sxs-lookup"><span data-stu-id="d69bf-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d69bf-183"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d69bf-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d69bf-184">DLL</span><span class="sxs-lookup"><span data-stu-id="d69bf-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69bf-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d69bf-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

