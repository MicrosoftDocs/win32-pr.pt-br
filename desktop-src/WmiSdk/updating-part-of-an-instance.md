---
description: Ocasionalmente, talvez você queira atualizar apenas parte de uma instância do.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Atualizando parte de uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782645"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="6a942-103">Atualizando parte de uma instância</span><span class="sxs-lookup"><span data-stu-id="6a942-103">Updating Part of an Instance</span></span>

<span data-ttu-id="6a942-104">Ocasionalmente, talvez você queira atualizar apenas parte de uma instância do.</span><span class="sxs-lookup"><span data-stu-id="6a942-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="6a942-105">Por exemplo, algumas instâncias têm um grande número de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6a942-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="6a942-106">Se você precisava atualizar um grande número dessas instâncias, poderá reduzir o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="6a942-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="6a942-107">Portanto, você pode optar por atualizar apenas parte da instância e, assim, reduzir a quantidade de informações que você deve enviar e recuperar de e para o WMI.</span><span class="sxs-lookup"><span data-stu-id="6a942-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="6a942-108">No entanto, o WMI não oferece suporte diretamente a operações de instância parcial nem a maioria dos provedores.</span><span class="sxs-lookup"><span data-stu-id="6a942-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="6a942-109">Portanto, se você escrever um aplicativo que usa operações de instância parcial, esteja preparado para que suas chamadas falhem com o **\_ provedor WBEM \_ e \_ não \_ compatível** ou o código de erro **WBEM \_ e \_ sem \_ suporte** em C++.</span><span class="sxs-lookup"><span data-stu-id="6a942-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="6a942-110">Em linguagens de script, os códigos de erro são **wbemErrProviderNotCapable** ou **wbemErrNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="6a942-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="6a942-111">No script, essa operação só é necessária para ajudar no desempenho ao atualizar uma ou duas propriedades graváveis em um número muito grande de objetos em uma empresa.</span><span class="sxs-lookup"><span data-stu-id="6a942-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="6a942-112">Caso contrário, as chamadas normais do VBScript para [**SWbemObject \_ . put**](swbemobject-put-.md) ou [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md), embora pareçam gravar o objeto inteiro, estão, na verdade, atualizando apenas as propriedades que o provedor tem habilitado para gravação.</span><span class="sxs-lookup"><span data-stu-id="6a942-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="6a942-113">O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a942-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="6a942-114">**Para solicitar uma atualização de instância parcial usando o PowerShell**</span><span class="sxs-lookup"><span data-stu-id="6a942-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="6a942-115">Recupere o caminho do objeto que você deseja atualizar.</span><span class="sxs-lookup"><span data-stu-id="6a942-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="6a942-116">Você pode descrever o caminho manualmente ou, caso contrário, consultar o objeto e, em seguida, recuperar a propriedade **\_ \_ Path** .</span><span class="sxs-lookup"><span data-stu-id="6a942-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="6a942-117">Configure uma tabela de hash listando os nomes das propriedades a serem atualizadas e use essa tabela de hash em uma chamada para [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="6a942-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="6a942-118">O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando C#.</span><span class="sxs-lookup"><span data-stu-id="6a942-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="6a942-119">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="6a942-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="6a942-120">**Para solicitar uma atualização de instância parcial usando C #**</span><span class="sxs-lookup"><span data-stu-id="6a942-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="6a942-121">Crie um novo objeto [ManagementObject](/dotnet/api/system.management.managementobject) que representa a instância específica a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="6a942-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="6a942-122">Defina o valor da propriedade com uma chamada para [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span><span class="sxs-lookup"><span data-stu-id="6a942-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="6a942-123">O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="6a942-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="6a942-124">**Para solicitar uma atualização de instância parcial usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="6a942-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="6a942-125">Crie um objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="6a942-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="6a942-126">Adicione os valores de extensão Put " \_ \_ colocar \_ extensões" e " \_ \_ colocar a solicitação de \_ \_ cliente ext" no objeto de \_ contexto usando o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="6a942-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="6a942-127">Configure uma matriz que liste os nomes das propriedades a serem atualizadas e adicione essa matriz ao objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) com o valor de extensão Put " \_ \_ Put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="6a942-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="6a942-128">Defina o parâmetro *iFlags* da chamada [**SWbemObject. put \_**](swbemobject-put-.md) para **wbemChangeFlagUpdateOnly**.</span><span class="sxs-lookup"><span data-stu-id="6a942-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="6a942-129">Sem esse sinalizador, a chamada falhará com um contexto inválido.</span><span class="sxs-lookup"><span data-stu-id="6a942-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="6a942-130">Passe o sinalizador e o objeto de contexto para o provedor no parâmetro *objwbemNamedValueSet* de [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).</span><span class="sxs-lookup"><span data-stu-id="6a942-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="6a942-131">O procedimento a seguir descreve como solicitar uma atualização de instância parcial usando C++.</span><span class="sxs-lookup"><span data-stu-id="6a942-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="6a942-132">**Para solicitar uma atualização de instância parcial usando C++**</span><span class="sxs-lookup"><span data-stu-id="6a942-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="6a942-133">Crie um objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="6a942-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="6a942-134">Um objeto de contexto é um objeto que o WMI usa para passar mais informações para um provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="6a942-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="6a942-135">Nesse caso, você está usando o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para instruir o provedor a aceitar atualizações de instância parcial.</span><span class="sxs-lookup"><span data-stu-id="6a942-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="6a942-136">Adicione os \_ \_ \_ valores nomeados "colocar extensões" e " \_ \_ colocar a solicitação de \_ \_ cliente ext \_ " ao objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="6a942-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="6a942-137">A tabela a seguir lista o significado de " \_ \_ colocar \_ extensões" e " \_ \_ colocar a solicitação do \_ \_ cliente ext \_ ".</span><span class="sxs-lookup"><span data-stu-id="6a942-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="6a942-138">Valor nomeado</span><span class="sxs-lookup"><span data-stu-id="6a942-138">Named value</span></span>                     | <span data-ttu-id="6a942-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a942-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6a942-140">" \_ \_ colocar \_ extensões"</span><span class="sxs-lookup"><span data-stu-id="6a942-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="6a942-141">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6a942-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="6a942-142">Um valor que indica que um ou mais dos outros valores de contexto foram especificados.</span><span class="sxs-lookup"><span data-stu-id="6a942-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="6a942-143">Isso permite uma verificação rápida do objeto de contexto dentro do provedor para determinar se atualizações de instância parcial estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="6a942-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="6a942-144">" \_ \_ colocar \_ solicitação do cliente ext. \_ \_ "</span><span class="sxs-lookup"><span data-stu-id="6a942-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="6a942-145">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6a942-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="6a942-146">Definido pelo cliente durante a solicitação inicial.</span><span class="sxs-lookup"><span data-stu-id="6a942-146">Set by the client during the initial request.</span></span> <span data-ttu-id="6a942-147">Esse valor é usado para evitar erros de reentrância.</span><span class="sxs-lookup"><span data-stu-id="6a942-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="6a942-148">Adicione as \_ \_ \_ Propriedades Put ext \_ estrito \_ , \_ \_ Put \_ ext \_ ou coloque o \_ \_ \_ Atomic ext \_ em qualquer combinação conforme necessário para o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com outra chamada para [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="6a942-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="6a942-149">A tabela a seguir lista o significado dos valores nomeados.</span><span class="sxs-lookup"><span data-stu-id="6a942-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="6a942-150">Valor nomeado</span><span class="sxs-lookup"><span data-stu-id="6a942-150">Named value</span></span>                   | <span data-ttu-id="6a942-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a942-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6a942-152">" \_ \_ colocar \_ \_ nulos estritos estendidos \_ "</span><span class="sxs-lookup"><span data-stu-id="6a942-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="6a942-153">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6a942-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="6a942-154">Indica que o cliente definiu intencionalmente as propriedades para **VT \_ NULL** e espera que a operação de gravação tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="6a942-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="6a942-155">Se o provedor não puder definir os valores como **NULL**, um erro deverá ser relatado.</span><span class="sxs-lookup"><span data-stu-id="6a942-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="6a942-156">" \_ \_ colocar \_ Propriedades ext. \_ "</span><span class="sxs-lookup"><span data-stu-id="6a942-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="6a942-157">[**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadeias de caracteres que contém uma lista de nomes de propriedade a serem atualizados.</span><span class="sxs-lookup"><span data-stu-id="6a942-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="6a942-158">Pode ser usado sozinho ou em combinação com " \_ \_ Put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="6a942-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="6a942-159">Os valores estão na instância que está sendo gravada.</span><span class="sxs-lookup"><span data-stu-id="6a942-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="6a942-160">" \_ \_ colocar \_ \_ Atomic ext"</span><span class="sxs-lookup"><span data-stu-id="6a942-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="6a942-161">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6a942-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="6a942-162">Indica que todas as atualizações devem ter sucesso simultaneamente (semântica atômica) ou o provedor deve reverter de volta.</span><span class="sxs-lookup"><span data-stu-id="6a942-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="6a942-163">Não pode haver nenhum sucesso parcial.</span><span class="sxs-lookup"><span data-stu-id="6a942-163">There can be no partial success.</span></span> <span data-ttu-id="6a942-164">Pode ser usado sozinha ou em combinação com outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="6a942-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="6a942-165">Defina o parâmetro *iFlags* como **\_ \_ \_ somente atualização do sinalizador WBEM**.</span><span class="sxs-lookup"><span data-stu-id="6a942-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="6a942-166">Sem esse sinalizador, a chamada falhará com um contexto inválido.</span><span class="sxs-lookup"><span data-stu-id="6a942-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="6a942-167">Passe o objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) em qualquer chamada [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) no parâmetro *pCtx* .</span><span class="sxs-lookup"><span data-stu-id="6a942-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="6a942-168">Passar o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) instrui o provedor para permitir atualizações parciais de instância.</span><span class="sxs-lookup"><span data-stu-id="6a942-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="6a942-169">Em uma atualização de instância completa, você definiria *pCtx* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6a942-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="6a942-170">O provedor poderá gravar todas as propriedades necessárias se o objeto de contexto presente na chamada não contiver " \_ \_ Put \_ Extensions".</span><span class="sxs-lookup"><span data-stu-id="6a942-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="6a942-171">Se " \_ \_ colocar \_ extensões" estiver presente no objeto de contexto, o WMI exigirá que o provedor obedeça a semântica da operação exatamente ou, caso contrário, falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="6a942-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="6a942-172">Para obter mais informações, consulte [manipulando mensagens de acesso negado em um provedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="6a942-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
