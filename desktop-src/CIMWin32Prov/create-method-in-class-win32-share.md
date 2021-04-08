---
description: Inicia o compartilhamento para um recurso de servidor.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Método Create da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920604"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="19969-103">Criar método da classe de \_ compartilhamento do Win32</span><span class="sxs-lookup"><span data-stu-id="19969-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="19969-104">O método **Create**   [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) inicia o compartilhamento para um recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="19969-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="19969-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="19969-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="19969-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="19969-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="19969-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19969-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="19969-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19969-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19969-109">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="19969-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-110">Caminho local do compartilhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="19969-110">Local path of the Windows share.</span></span>

<span data-ttu-id="19969-111">Exemplo, "C: \\ arquivos de programas".</span><span class="sxs-lookup"><span data-stu-id="19969-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="19969-112">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="19969-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-113">Passa o alias para um caminho configurado como um compartilhamento em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="19969-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="19969-114">Exemplo, "público".</span><span class="sxs-lookup"><span data-stu-id="19969-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="19969-115">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="19969-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-116">Passa o tipo de recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="19969-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="19969-117">Os tipos incluem unidades de disco, filas de impressão, IPC (comunicações entre processos) e dispositivos gerais.</span><span class="sxs-lookup"><span data-stu-id="19969-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="19969-118">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="19969-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="19969-119">**Unidade de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="19969-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="19969-120">**Fila de impressão** (1)</span><span class="sxs-lookup"><span data-stu-id="19969-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="19969-121">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="19969-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="19969-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="19969-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="19969-123">**Administrador da unidade de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="19969-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="19969-124">**Administrador da fila de impressão** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="19969-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="19969-125">**Administrador do dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="19969-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="19969-126">**Administrador de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="19969-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="19969-127">*MaximumAllowed* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19969-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-128">Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="19969-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="19969-129">Exemplo: 10.</span><span class="sxs-lookup"><span data-stu-id="19969-129">Example: 10.</span></span> <span data-ttu-id="19969-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="19969-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="19969-131">*Descrição* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19969-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-132">Comentário opcional para descrever o recurso que está sendo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="19969-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="19969-133">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="19969-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="19969-134">*Senha* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19969-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-135">Senha (quando o servidor está sendo executado com segurança em nível de compartilhamento) para o recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="19969-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="19969-136">Se o servidor estiver sendo executado com segurança em nível de usuário, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="19969-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="19969-137">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="19969-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="19969-138">*Acesso* \[ ao em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19969-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19969-139">Descritor de segurança para permissões de nível de usuário.</span><span class="sxs-lookup"><span data-stu-id="19969-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="19969-140">Um descritor de segurança contém informações sobre as permissões, o proprietário e os recursos de acesso do recurso.</span><span class="sxs-lookup"><span data-stu-id="19969-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="19969-141">Se esse parâmetro não for fornecido ou for **nulo**, todos têm acesso de leitura ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="19969-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="19969-142">Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) e [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="19969-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19969-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19969-143">Return value</span></span>

<span data-ttu-id="19969-144">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="19969-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="19969-145">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="19969-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="19969-146">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="19969-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="19969-147">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="19969-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="19969-148">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="19969-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="19969-149">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="19969-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="19969-150">**Nome inválido** (9)</span><span class="sxs-lookup"><span data-stu-id="19969-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="19969-151">**Nível inválido** (10)</span><span class="sxs-lookup"><span data-stu-id="19969-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="19969-152">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="19969-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="19969-153">**Compartilhamento duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="19969-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="19969-154">**Caminho Redirecionado** (23)</span><span class="sxs-lookup"><span data-stu-id="19969-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="19969-155">**Dispositivo ou diretório desconhecido** (24)</span><span class="sxs-lookup"><span data-stu-id="19969-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="19969-156">**Nome de rede não encontrado** (25)</span><span class="sxs-lookup"><span data-stu-id="19969-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="19969-157">**Outro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="19969-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="19969-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="19969-158">Remarks</span></span>

<span data-ttu-id="19969-159">**Create** é um método estático.</span><span class="sxs-lookup"><span data-stu-id="19969-159">**Create** is a static method.</span></span>

<span data-ttu-id="19969-160">Somente os membros do grupo local Administradores ou operadores de contas, ou aqueles com associação de grupo de operador de servidor, impressão ou comunicação, podem executar a **criação** com êxito.</span><span class="sxs-lookup"><span data-stu-id="19969-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="19969-161">O operador Print só pode adicionar filas de impressora.</span><span class="sxs-lookup"><span data-stu-id="19969-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="19969-162">O operador de comunicação só pode adicionar filas de dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="19969-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="19969-163">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19969-163">Examples</span></span>

<span data-ttu-id="19969-164">O exemplo de [exportar e importar fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) do PowerShell exporta e importa compartilhamentos de arquivos e define permissões de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="19969-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="19969-165">Da mesma forma, o exemplo [criar um compartilhamento e definir permissões](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) também cria um novo compartilhamento e define as permissões de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="19969-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="19969-166">O código do PowerShell a seguir cria um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="19969-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="19969-167">O exemplo de código anterior retorna o seguinte:</span><span class="sxs-lookup"><span data-stu-id="19969-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="19969-168">O exemplo de código C a seguir \# descreve como chamar o método Create.</span><span class="sxs-lookup"><span data-stu-id="19969-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="19969-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19969-169">Requirements</span></span>



| <span data-ttu-id="19969-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="19969-170">Requirement</span></span> | <span data-ttu-id="19969-171">Valor</span><span class="sxs-lookup"><span data-stu-id="19969-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19969-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19969-172">Minimum supported client</span></span><br/> | <span data-ttu-id="19969-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19969-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19969-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19969-174">Minimum supported server</span></span><br/> | <span data-ttu-id="19969-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19969-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19969-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="19969-176">Namespace</span></span><br/>                | <span data-ttu-id="19969-177">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="19969-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19969-178">MOF</span><span class="sxs-lookup"><span data-stu-id="19969-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19969-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19969-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19969-180">DLL</span><span class="sxs-lookup"><span data-stu-id="19969-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19969-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19969-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19969-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="19969-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="19969-183">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19969-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="19969-184">**Compartilhamento do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="19969-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

