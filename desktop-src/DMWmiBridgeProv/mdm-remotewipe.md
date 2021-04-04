---
title: Classe MDM_RemoteWipe
description: A \_ classe MDM RemoteWipe permite um apagamento remoto de um dispositivo.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- Classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008901"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="f1c64-105">\_Classe RemoteWipe do MDM</span><span class="sxs-lookup"><span data-stu-id="f1c64-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="f1c64-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f1c64-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f1c64-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f1c64-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f1c64-108">A classe **MDM \_ RemoteWipe** permite um apagamento remoto de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c64-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="f1c64-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f1c64-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c64-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1c64-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="f1c64-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f1c64-111">Members</span></span>

<span data-ttu-id="f1c64-112">A classe **MDM \_ RemoteWipe** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1c64-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="f1c64-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1c64-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1c64-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c64-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1c64-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1c64-115">Methods</span></span>

<span data-ttu-id="f1c64-116">A classe **MDM \_ RemoteWipe** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f1c64-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="f1c64-117">Método</span><span class="sxs-lookup"><span data-stu-id="f1c64-117">Method</span></span>                                              | <span data-ttu-id="f1c64-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c64-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="f1c64-119">**doWipeMethod**</span><span class="sxs-lookup"><span data-stu-id="f1c64-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="f1c64-120">Dispara o dispositivo para iniciar o apagamento remoto.</span><span class="sxs-lookup"><span data-stu-id="f1c64-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1c64-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c64-121">Properties</span></span>

<span data-ttu-id="f1c64-122">A classe **MDM \_ RemoteWipe** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1c64-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1c64-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1c64-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c64-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1c64-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c64-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1c64-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1c64-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1c64-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1c64-127">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="f1c64-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="f1c64-128">Para essa classe, a cadeia de caracteres é "RemoteWipe".</span><span class="sxs-lookup"><span data-stu-id="f1c64-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="f1c64-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f1c64-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1c64-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1c64-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1c64-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1c64-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1c64-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1c64-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1c64-133">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="f1c64-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="f1c64-134">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="f1c64-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="f1c64-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f1c64-135">Example</span></span>

<span data-ttu-id="f1c64-136">O exemplo a seguir demonstra como usar o RemoteWipe e invocar o doWipeMethod.</span><span class="sxs-lookup"><span data-stu-id="f1c64-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="f1c64-137">Este exemplo deve ser executado em usuário do sistema local.</span><span class="sxs-lookup"><span data-stu-id="f1c64-137">This example must be executed under local system user.</span></span> <span data-ttu-id="f1c64-138">Para fazer isso, baixe a ferramenta PsExec do <https://technet.microsoft.com/sysinternals/bb897553.aspx> e execute a `psexec.exe -i -s cmd.exe` partir de um prompt de comando de administrador elevado.</span><span class="sxs-lookup"><span data-stu-id="f1c64-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="f1c64-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c64-139">Requirements</span></span>



| <span data-ttu-id="f1c64-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c64-140">Requirement</span></span> | <span data-ttu-id="f1c64-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f1c64-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c64-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c64-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c64-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f1c64-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1c64-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c64-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c64-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f1c64-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f1c64-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1c64-146">Namespace</span></span><br/>                | <span data-ttu-id="f1c64-147">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f1c64-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f1c64-148">MOF</span><span class="sxs-lookup"><span data-stu-id="f1c64-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1c64-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1c64-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1c64-150">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c64-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c64-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1c64-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c64-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1c64-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c64-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="f1c64-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

