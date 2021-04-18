---
description: Você pode usar os métodos do objeto SWbemLocator para obter um objeto SWbemServices que representa uma conexão com um namespace em um computador local ou em um computador host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objeto SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813340"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="fd1bc-103">Objeto SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="fd1bc-103">SWbemLocator object</span></span>

<span data-ttu-id="fd1bc-104">Você pode usar os métodos do objeto **SWbemLocator** para obter um objeto [**SWbemServices**](swbemservices.md) que representa uma conexão com um namespace em um computador local ou em um computador host remoto.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="fd1bc-105">Em seguida, você pode usar os métodos do objeto **SWbemServices** para acessar o WMI.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="fd1bc-106">Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="fd1bc-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="fd1bc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fd1bc-107">Members</span></span>

<span data-ttu-id="fd1bc-108">O objeto **SWbemLocator** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fd1bc-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="fd1bc-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd1bc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd1bc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fd1bc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd1bc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd1bc-111">Methods</span></span>

<span data-ttu-id="fd1bc-112">O objeto **SWbemLocator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="fd1bc-113">Método</span><span class="sxs-lookup"><span data-stu-id="fd1bc-113">Method</span></span>                                              | <span data-ttu-id="fd1bc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd1bc-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="fd1bc-115">**ConnectServer**</span><span class="sxs-lookup"><span data-stu-id="fd1bc-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="fd1bc-116">Conecta-se ao WMI no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fd1bc-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fd1bc-117">Properties</span></span>

<span data-ttu-id="fd1bc-118">O objeto **SWbemLocator** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="fd1bc-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fd1bc-119">Property</span></span>                                                | <span data-ttu-id="fd1bc-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fd1bc-120">Access type</span></span>          | <span data-ttu-id="fd1bc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd1bc-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="fd1bc-122">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="fd1bc-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="fd1bc-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fd1bc-123">Read-only</span></span><br/> | <span data-ttu-id="fd1bc-124">Usado para ler ou alterar as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd1bc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd1bc-125">Remarks</span></span>

<span data-ttu-id="fd1bc-126">Na parte superior do modelo de objeto da biblioteca de scripts do WMI está o objeto SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="fd1bc-127">SWbemLocator é usado para estabelecer uma conexão autenticada com um namespace WMI, assim como a função VBScript GetObject e o moniker WMI "winmgmts:" são usados para estabelecer uma conexão autenticada com o WMI.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="fd1bc-128">No entanto, o SWbemLocator foi projetado para abordar dois cenários de script específicos que não podem ser executados usando GetObject e o moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="fd1bc-129">Você deve usar SWbemLocator se precisar:</span><span class="sxs-lookup"><span data-stu-id="fd1bc-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="fd1bc-130">Forneça credenciais de usuário e senha para se conectar ao WMI em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="fd1bc-131">O moniker WMI usado com a função GetObject não inclui um mecanismo para especificar credenciais.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="fd1bc-132">A maioria das atividades do WMI (incluindo todas as que são executadas em computadores remotos) exige direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="fd1bc-133">Se você normalmente faz logon usando uma conta de usuário comum em vez de uma conta de administrador, não poderá executar a maioria das tarefas do WMI, a menos que execute o script em credenciais alternativas.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="fd1bc-134">Conecte-se ao WMI se você estiver executando um script WMI de dentro de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="fd1bc-135">Você não pode usar a função GetObject ao executar scripts inseridos em uma página HTML porque o Internet Explorer não permite o uso de GetObject por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="fd1bc-136">Além disso, talvez você queira usar o SWbemLocator para se conectar ao WMI se encontrar a cadeia de conexão do WMI usada com GetObject confuso ou difícil.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="fd1bc-137">Você usa CreateObject em vez de GetObject para criar uma referência a SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="fd1bc-138">Para criar a referência, você deve passar a função CreateObject do identificador programático SWbemLocator (ProgID) "WbemScripting. SWbemLocator", conforme mostrado na linha 2 no exemplo de script a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="fd1bc-139">Depois de obter uma referência a um objeto SWbemLocator, você chama o método ConnectServer para se conectar ao WMI e obter uma referência a um objeto SWbemServices.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="fd1bc-140">Isso é demonstrado na linha 3 do script a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="fd1bc-141">Para executar um script em credenciais alternativas, inclua o nome de usuário e a senha como parâmetros adicionais passados para ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="fd1bc-142">Por exemplo, esse script é executado sob as credenciais de um usuário chamado kenmyer, com a senha homerj.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="fd1bc-143">Você também pode usar o formato de nome de usuário de domínio \\ para especificar um nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="fd1bc-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fd1bc-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="fd1bc-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd1bc-145">Examples</span></span>

<span data-ttu-id="fd1bc-146">O exemplo do PowerShell a seguir usa **SWbemLocator** para se conectar a um servidor.</span><span class="sxs-lookup"><span data-stu-id="fd1bc-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="fd1bc-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd1bc-147">Requirements</span></span>



| <span data-ttu-id="fd1bc-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1bc-148">Requirement</span></span> | <span data-ttu-id="fd1bc-149">Valor</span><span class="sxs-lookup"><span data-stu-id="fd1bc-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1bc-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd1bc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1bc-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd1bc-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd1bc-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd1bc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1bc-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd1bc-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd1bc-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd1bc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1bc-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1bc-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd1bc-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fd1bc-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd1bc-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd1bc-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd1bc-158">DLL</span><span class="sxs-lookup"><span data-stu-id="fd1bc-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd1bc-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd1bc-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fd1bc-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="fd1bc-160">CLSID</span></span><br/>                    | <span data-ttu-id="fd1bc-161">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="fd1bc-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="fd1bc-162">IID</span><span class="sxs-lookup"><span data-stu-id="fd1bc-162">IID</span></span><br/>                      | <span data-ttu-id="fd1bc-163">ISWbemLocator de IID \_</span><span class="sxs-lookup"><span data-stu-id="fd1bc-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="fd1bc-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd1bc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1bc-165">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="fd1bc-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




