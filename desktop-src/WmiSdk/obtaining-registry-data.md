---
description: Você pode obter ou modificar dados do registro usando a classe WMI StdRegProv e seus métodos.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtendo dados do registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791510"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="f7b0c-103">Obtendo dados do registro</span><span class="sxs-lookup"><span data-stu-id="f7b0c-103">Obtaining Registry Data</span></span>

<span data-ttu-id="f7b0c-104">Você pode obter ou modificar dados do registro usando a classe WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e seus métodos.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="f7b0c-105">Ao usar o utilitário regedit para exibir e alterar valores de registro no computador local, o **StdRegProv** permite que você use um script ou aplicativo para automatizar essas atividades no computador local e nos computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="f7b0c-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contém métodos para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7b0c-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="f7b0c-107">Verificar as permissões de acesso de um usuário</span><span class="sxs-lookup"><span data-stu-id="f7b0c-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="f7b0c-108">Criar, enumerar e excluir chaves do registro</span><span class="sxs-lookup"><span data-stu-id="f7b0c-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="f7b0c-109">Criar, enumerar e excluir subchaves ou valores nomeados</span><span class="sxs-lookup"><span data-stu-id="f7b0c-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="f7b0c-110">Ler, gravar e excluir valores de dados</span><span class="sxs-lookup"><span data-stu-id="f7b0c-110">Read, write, and delete data values</span></span>

<span data-ttu-id="f7b0c-111">Os dados do registro são organizados por subárvores, chaves e subchaves aninhadas sob uma chave de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="f7b0c-112">Os valores de dados reais são chamados de entradas ou valores nomeados.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="f7b0c-113">As subárvores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7b0c-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="f7b0c-114">**HKEY \_ CLASSES \_ raiz** (abreviadas como **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="f7b0c-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="f7b0c-115">**HKEY \_ \_usuário atual** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="f7b0c-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="f7b0c-116">**HKEY \_ \_computador local** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="f7b0c-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="f7b0c-117">**usuários de HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="f7b0c-118">**\_configuração atual de hKey \_**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="f7b0c-119">Por exemplo, na entrada do registro **HKEY** \\ **software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, a subárvore hKey é **software**; as subchaves são **Microsoft** e **DirectX**; e a entrada de valor nomeado é **InstalledVersion**.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="f7b0c-120">Um [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ocorre quando ocorre uma alteração em uma chave específica, mas a entrada não identifica como os valores são alterados nem o evento é disparado por alterações abaixo da chave especificada.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="f7b0c-121">Para identificar alterações em qualquer lugar em uma estrutura de chave hierárquica, use o [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), que não retorna valores específicos ou alterações de chave que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="f7b0c-122">Para obter uma alteração de valor de entrada específica, use o [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)e, em seguida, leia a entrada para obter um valor de linha de base.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="f7b0c-123">O [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) só tem métodos que podem ser chamados de C++ ou script, que é diferente da estrutura de classes do Win32.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="f7b0c-124">O exemplo de código a seguir mostra como usar o método [**StdRegProv. EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) para listar todas as subchaves de software da Microsoft na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="f7b0c-125">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="f7b0c-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tem métodos diferentes para ler os vários tipos de dados de valor de entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="f7b0c-127">Se a entrada tiver valores desconhecidos, você poderá chamar [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para listá-los.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="f7b0c-128">A tabela a seguir lista a correspondência entre os métodos **StdRegProv** e os tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="f7b0c-129">Método</span><span class="sxs-lookup"><span data-stu-id="f7b0c-129">Method</span></span>                                                                                  | <span data-ttu-id="f7b0c-130">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f7b0c-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="f7b0c-131">**Getbinaryvalue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="f7b0c-132">**\_binário reg**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="f7b0c-133">**Getdwordvalue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="f7b0c-134">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="f7b0c-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="f7b0c-136">**REG \_ expande \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="f7b0c-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="f7b0c-138">**REG \_ multi \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="f7b0c-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="f7b0c-140">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="f7b0c-141">A tabela a seguir lista os métodos correspondentes para criar novas chaves ou valores, ou alterar os existentes.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="f7b0c-142">Método</span><span class="sxs-lookup"><span data-stu-id="f7b0c-142">Method</span></span>                                                                                  | <span data-ttu-id="f7b0c-143">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f7b0c-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="f7b0c-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="f7b0c-145">**\_binário reg**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="f7b0c-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="f7b0c-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="f7b0c-148">**SetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="f7b0c-149">**REG \_ expande \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="f7b0c-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="f7b0c-151">**REG \_ multi \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="f7b0c-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="f7b0c-153">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f7b0c-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="f7b0c-154">O exemplo a seguir mostra como ler a lista de fontes para o log de eventos do sistema da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="f7b0c-155">**HKEY \_ Sistema de \_ máquina local** \\ **sistema** de controle do \\ **conjunto de controles atual** \\  \\  \\ **sistemas** log de eventos</span><span class="sxs-lookup"><span data-stu-id="f7b0c-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="f7b0c-156">Observe que os itens no valor de multistring são tratados como uma coleção ou matriz.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="f7b0c-157">O provedor de registro é hospedado no LocalService — não no LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="f7b0c-158">Portanto, obter informações remotamente da subárvore **HKEY \_ Current \_ User** não é possível.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="f7b0c-159">No entanto, os scripts executados no computador local ainda podem acessar o **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="f7b0c-160">Você pode definir o modelo de hospedagem para LocalSystem em um computador remoto, mas isso é um risco de segurança, pois o registro no computador remoto é vulnerável ao acesso hostil.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="f7b0c-161">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f7b0c-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f7b0c-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7b0c-162">Examples</span></span>

<span data-ttu-id="f7b0c-163">O exemplo de código VBScript [ler um valor de registro binário](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) na galeria do TechNet usa o WMI para ler um valor de registro binário.</span><span class="sxs-lookup"><span data-stu-id="f7b0c-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7b0c-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7b0c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7b0c-165">Tarefas do WMI: registro</span><span class="sxs-lookup"><span data-stu-id="f7b0c-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
