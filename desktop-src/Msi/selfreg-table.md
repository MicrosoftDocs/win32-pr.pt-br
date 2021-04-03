---
description: A tabela SelfReg contém informações sobre os módulos que precisam ser registrados automaticamente.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabela SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663370"
---
# <a name="selfreg-table"></a><span data-ttu-id="92d09-103">Tabela SelfReg</span><span class="sxs-lookup"><span data-stu-id="92d09-103">SelfReg Table</span></span>

<span data-ttu-id="92d09-104">A tabela SelfReg contém informações sobre os módulos que precisam ser registrados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92d09-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="92d09-105">O instalador chama a função [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante a instalação do módulo; Ele chama [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante a desinstalação do módulo.</span><span class="sxs-lookup"><span data-stu-id="92d09-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="92d09-106">O instalador não registra automaticamente arquivos EXE.</span><span class="sxs-lookup"><span data-stu-id="92d09-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="92d09-107">A tabela SelfReg tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="92d09-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="92d09-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="92d09-108">Column</span></span> | <span data-ttu-id="92d09-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="92d09-109">Type</span></span>                         | <span data-ttu-id="92d09-110">Chave</span><span class="sxs-lookup"><span data-stu-id="92d09-110">Key</span></span> | <span data-ttu-id="92d09-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="92d09-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="92d09-112">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="92d09-112">File\_</span></span> | [<span data-ttu-id="92d09-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="92d09-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="92d09-114">S</span><span class="sxs-lookup"><span data-stu-id="92d09-114">Y</span></span>   | <span data-ttu-id="92d09-115">N</span><span class="sxs-lookup"><span data-stu-id="92d09-115">N</span></span>        |
| <span data-ttu-id="92d09-116">Custo</span><span class="sxs-lookup"><span data-stu-id="92d09-116">Cost</span></span>   | [<span data-ttu-id="92d09-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="92d09-117">Integer</span></span>](integer.md)       | <span data-ttu-id="92d09-118">N</span><span class="sxs-lookup"><span data-stu-id="92d09-118">N</span></span>   | <span data-ttu-id="92d09-119">S</span><span class="sxs-lookup"><span data-stu-id="92d09-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="92d09-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="92d09-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="92d09-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="92d09-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="92d09-122">Chave externa na primeira coluna da tabela de [arquivos](file-table.md) que indica o módulo que precisa ser registrado.</span><span class="sxs-lookup"><span data-stu-id="92d09-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="92d09-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Custo</span><span class="sxs-lookup"><span data-stu-id="92d09-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="92d09-124">O custo de registrar o módulo em bytes.</span><span class="sxs-lookup"><span data-stu-id="92d09-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="92d09-125">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="92d09-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92d09-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="92d09-126">Remarks</span></span>

<span data-ttu-id="92d09-127">Os autores do pacote de instalação são altamente aconselhados em relação ao uso de auto-registro.</span><span class="sxs-lookup"><span data-stu-id="92d09-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="92d09-128">Em vez disso, eles devem registrar módulos criando uma ou mais tabelas fornecidas pelo instalador para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="92d09-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="92d09-129">Para obter mais informações, consulte [grupo de tabelas do registro](registry-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="92d09-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="92d09-130">Muitos dos benefícios de ter um serviço do instalador central são perdidos com o auto-registro porque as rotinas de Autoregistro tendem a ocultar informações de configuração críticas.</span><span class="sxs-lookup"><span data-stu-id="92d09-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="92d09-131">Os motivos para evitar o auto-registro incluem:</span><span class="sxs-lookup"><span data-stu-id="92d09-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="92d09-132">A reversão de uma instalação com módulos autoregistrados não pode ser feita com segurança usando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque não há nenhuma maneira de informar se as chaves autoregistradas são usadas por outro recurso ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92d09-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="92d09-133">A capacidade de usar o anúncio será reduzida se o registro do servidor de extensão ou de classe for executado em rotinas de auto-registro.</span><span class="sxs-lookup"><span data-stu-id="92d09-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="92d09-134">O instalador manipula automaticamente as chaves de HKCR nas tabelas do registro para instalações por usuário ou por computador.</span><span class="sxs-lookup"><span data-stu-id="92d09-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="92d09-135">Atualmente, as rotinas de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) não dão suporte à noção de uma chave de HKCR por usuário.</span><span class="sxs-lookup"><span data-stu-id="92d09-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="92d09-136">Se vários usuários estiverem usando um aplicativo AutoRegistrado no mesmo computador, cada usuário deverá instalar o aplicativo na primeira vez que executá-lo.</span><span class="sxs-lookup"><span data-stu-id="92d09-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="92d09-137">Caso contrário, o instalador não poderá determinar facilmente que as chaves de Registro HKCU apropriadas existam.</span><span class="sxs-lookup"><span data-stu-id="92d09-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="92d09-138">A [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) pode ter acesso negado a recursos de rede, como bibliotecas de tipos, se um componente for especificado como Run-from-Source e estiver listado na tabela selfreg.</span><span class="sxs-lookup"><span data-stu-id="92d09-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="92d09-139">Isso pode fazer com que a instalação do componente falhe durante uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="92d09-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="92d09-140">As DLLs de registro automático são mais suscetíveis a erros de codificação porque o novo código necessário para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) é normalmente diferente para cada DLL.</span><span class="sxs-lookup"><span data-stu-id="92d09-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="92d09-141">Em vez disso, use as tabelas do registro no banco de dados para aproveitar o código existente fornecido pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="92d09-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="92d09-142">As DLLs de registro automático podem, às vezes, se vincular a DLLs auxiliares que não estão presentes ou estão na versão errada.</span><span class="sxs-lookup"><span data-stu-id="92d09-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="92d09-143">Por outro lado, o instalador pode registrar as DLLs usando as tabelas do registro sem dependência no estado atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="92d09-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="92d09-144">Não é possível especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de Autoregistro usando as ações [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="92d09-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="92d09-145">Consulte [especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="92d09-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="92d09-146">Validação</span><span class="sxs-lookup"><span data-stu-id="92d09-146">Validation</span></span>

<dl>

[<span data-ttu-id="92d09-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="92d09-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="92d09-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="92d09-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="92d09-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="92d09-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
