---
description: A função RegOpenUserClassesRoot fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Exibição mesclada de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769168"
---
# <a name="merged-view-of-hkey_classes_root"></a><span data-ttu-id="7ad41-103">Exibição mesclada da \_ raiz de classes hKey \_</span><span class="sxs-lookup"><span data-stu-id="7ad41-103">Merged View of HKEY\_CLASSES\_ROOT</span></span>

<span data-ttu-id="7ad41-104">A função [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="7ad41-104">The [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) function provides a merged view for processes, such as services, that are dealing with clients other than the interactive user.</span></span> <span data-ttu-id="7ad41-105">Nesse caso, a chave **de \_ \_ raiz de classes hKey** fornece uma exibição do registro que mescla as informações de **\_ \_ \\ \\ classes de software de computador local hKey** com as informações de **HKEY \_ Current \_ user \\ software \\ classes**.</span><span class="sxs-lookup"><span data-stu-id="7ad41-105">In this case, the **HKEY\_CLASSES\_ROOT** key provides a view of the registry that merges the information from **HKEY\_LOCAL\_MACHINE\\Software\\Classes** with the information from **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span>

<span data-ttu-id="7ad41-106">O sistema usa as seguintes regras para mesclar informações das duas fontes:</span><span class="sxs-lookup"><span data-stu-id="7ad41-106">The system uses the following rules to merge information from the two sources:</span></span>

-   <span data-ttu-id="7ad41-107">A exibição mesclada inclui todas as subchaves da chave do **HKEY \_ Current \_ user \\ software \\ classes** .</span><span class="sxs-lookup"><span data-stu-id="7ad41-107">The merged view includes all subkeys of the **HKEY\_CURRENT\_USER\\Software\\Classes** key.</span></span>
-   <span data-ttu-id="7ad41-108">A exibição mesclada inclui todas as subchaves imediatas da chave de **\_ classes de \_ \\ software \\ da máquina local hKey** que não duplicam as subchaves das **\_ classes HKEY Current \_ user \\ software \\**.</span><span class="sxs-lookup"><span data-stu-id="7ad41-108">The merged view includes all immediate subkeys of the **HKEY\_LOCAL\_MACHINE\\Software\\Classes** key that do not duplicate the subkeys of **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span>
-   <span data-ttu-id="7ad41-109">No final deste tópico há uma lista de subchaves encontradas em **HKEY \_ local \_ Machine \\ software \\ classes** e **HKEY \_ Current \_ user \\ software \\ classes**.</span><span class="sxs-lookup"><span data-stu-id="7ad41-109">At the end of this topic is a list of subkeys that are found in both **HKEY\_LOCAL\_MACHINE\\Software\\Classes** and **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span> <span data-ttu-id="7ad41-110">As subchaves imediatas dessas chaves da árvore do **\_ \_ computador local hKey** serão incluídas na exibição mesclada somente se não forem duplicatas de subchaves imediatas da árvore de **\_ \_ usuário atual do hKey** .</span><span class="sxs-lookup"><span data-stu-id="7ad41-110">The immediate subkeys of these keys from the **HKEY\_LOCAL\_MACHINE** tree are included in the merged view only if they are not duplicates of immediate subkeys from the **HKEY\_CURRENT\_USER** tree.</span></span> <span data-ttu-id="7ad41-111">A exibição mesclada não inclui o conteúdo **do \_ \_ computador local hKey** de subchaves duplicadas.</span><span class="sxs-lookup"><span data-stu-id="7ad41-111">The merged view does not include the **HKEY\_LOCAL\_MACHINE** contents of duplicate subkeys.</span></span>

<span data-ttu-id="7ad41-112">Se um aplicativo for executado com direitos de administrador e o controle de conta de usuário estiver desabilitado, o tempo de execução do COM ignorará a configuração de COM por usuário e acessará apenas a configuração de COM por computador.</span><span class="sxs-lookup"><span data-stu-id="7ad41-112">If an application is run with administrator rights and User Account Control is disabled, the COM runtime ignores per-user COM configuration and accesses only per-machine COM configuration.</span></span> <span data-ttu-id="7ad41-113">Os aplicativos que exigem direitos de administrador devem registrar objetos COM dependentes durante a instalação para o repositório de configuração COM por máquina (**HKEY \_ local \_ Machine \\ software \\ classes**).</span><span class="sxs-lookup"><span data-stu-id="7ad41-113">Applications that require administrator rights should register dependent COM objects during installation to the per-machine COM configuration store (**HKEY\_LOCAL\_MACHINE\\Software\\Classes**).</span></span> <span data-ttu-id="7ad41-114">Para obter mais informações, consulte [AC: UAC: configuração de Per-User com](/previous-versions/bb756926(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7ad41-114">For more information, see [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).</span></span>

<span data-ttu-id="7ad41-115">**Windows Server 2003 e Windows XP/2000:** Os aplicativos podem registrar objetos COM dependentes no repositório de configuração COM por máquina ou por usuário (**HKEY \_ local \_ Machine \\ software \\ classes** ou **HKEY \_ Current \_ user \\ software \\ classes**).</span><span class="sxs-lookup"><span data-stu-id="7ad41-115">**Windows Server 2003 and Windows XP/2000:** Applications can register dependent COM objects to either the per-machine or per-user COM configuration store (**HKEY\_LOCAL\_MACHINE\\Software\\Classes** or **HKEY\_CURRENT\_USER\\Software\\Classes**).</span></span>

<span data-ttu-id="7ad41-116">O exemplo a seguir mostra um conjunto de subchaves **no \_ \_ computador local hKey** e o **HKEY \_ Current \_ User** Keys e a exibição mesclada resultante da **\_ \_ raiz de classes hKey**.</span><span class="sxs-lookup"><span data-stu-id="7ad41-116">The following example shows a set of subkeys under the **HKEY\_LOCAL\_MACHINE** and **HKEY\_CURRENT\_USER** keys and the resulting merged view of **HKEY\_CLASSES\_ROOT**.</span></span>

<span data-ttu-id="7ad41-117">**HKEY \_ \_Classes de \\ software \\ de computador local**    **CLSID**       *2*       *4*          **InprocServer32**          **LocalServer32**       *7*</span><span class="sxs-lookup"><span data-stu-id="7ad41-117">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*</span></span>

<span data-ttu-id="7ad41-118">**HKEY \_ \_Classes de \\ software \\ de usuário atuais**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**</span><span class="sxs-lookup"><span data-stu-id="7ad41-118">**HKEY\_CURRENT\_USER\\Software\\Classes**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**</span></span>

<span data-ttu-id="7ad41-119">**HKEY \_ CLASSES \_ raiz**    **CLSID**       *1*       *2*       *4*          **InprocServer32**          **LocalServer**          **LocalServer32**       *6*       *7*       *10*          **LocalServer**</span><span class="sxs-lookup"><span data-stu-id="7ad41-119">**HKEY\_CLASSES\_ROOT**    **CLSID**       *1*       *2*       *4*          **inprocserver32**          **localserver**          **localserver32**       *6*       *7*       *10*          **localserver**</span></span>

<span data-ttu-id="7ad41-120">As seguintes subchaves são encontradas em **HKEY \_ local \_ Machine \\ software \\ classes** e **HKEY \_ Current \_ user \\ software \\ classes**.</span><span class="sxs-lookup"><span data-stu-id="7ad41-120">The following subkeys are found in both **HKEY\_LOCAL\_MACHINE\\Software\\Classes** and **HKEY\_CURRENT\_USER\\Software\\Classes**.</span></span> <span data-ttu-id="7ad41-121">Na árvore **do \_ \_ computador local hKey** , as subchaves imediatas dessas chaves serão incluídas na exibição mesclada somente se não forem duplicatas das subchaves imediatas da árvore de **\_ \_ usuário atual do hKey** .</span><span class="sxs-lookup"><span data-stu-id="7ad41-121">From the **HKEY\_LOCAL\_MACHINE** tree, the immediate subkeys of these keys are included in the merged view only if they are not duplicates of immediate subkeys from the **HKEY\_CURRENT\_USER** tree.</span></span> <span data-ttu-id="7ad41-122">A exibição mesclada não inclui o conteúdo **do \_ \_ computador local hKey** de subchaves duplicadas.</span><span class="sxs-lookup"><span data-stu-id="7ad41-122">The merged view does not include the **HKEY\_LOCAL\_MACHINE** contents of duplicate subkeys.</span></span>

<span data-ttu-id="7ad41-123">**\**_ _*\*\\ shellex**</span><span class="sxs-lookup"><span data-stu-id="7ad41-123">**\**_ _*\*\\shellex**</span></span>  
<span data-ttu-id="7ad41-124">**\*\\shellex \\ ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-124">**\*\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="7ad41-125">**\*\\shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-125">**\*\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="7ad41-126">**AppID**</span><span class="sxs-lookup"><span data-stu-id="7ad41-126">**AppID**</span></span>  
<span data-ttu-id="7ad41-127">**ClsID**</span><span class="sxs-lookup"><span data-stu-id="7ad41-127">**ClsID**</span></span>  
<span data-ttu-id="7ad41-128">**Categorias de componentes**</span><span class="sxs-lookup"><span data-stu-id="7ad41-128">**Component Categories**</span></span>  
<span data-ttu-id="7ad41-129">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="7ad41-129">**Drive**</span></span>  
<span data-ttu-id="7ad41-130">**Shellex da unidade \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-130">**Drive\\shellex**</span></span>  
<span data-ttu-id="7ad41-131">**Unidade \\ shellex \\ ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-131">**Drive\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="7ad41-132">**Unidade \\ shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-132">**Drive\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="7ad41-133">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="7ad41-133">**FileType**</span></span>  
<span data-ttu-id="7ad41-134">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="7ad41-134">**Folder**</span></span>  
<span data-ttu-id="7ad41-135">**Shellex da pasta \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-135">**Folder\\shellex**</span></span>  
<span data-ttu-id="7ad41-136">**Pasta \\ shellex \\ ColumnHandler**</span><span class="sxs-lookup"><span data-stu-id="7ad41-136">**Folder\\shellex\\ColumnHandler**</span></span>  
<span data-ttu-id="7ad41-137">**Pasta \\ shellex \\ ContextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-137">**Folder\\shellex\\ContextMenuHandlers**</span></span>  
<span data-ttu-id="7ad41-138">**Pasta \\ shellex \\ ExtShellFolderViews**</span><span class="sxs-lookup"><span data-stu-id="7ad41-138">**Folder\\shellex\\ExtShellFolderViews**</span></span>  
<span data-ttu-id="7ad41-139">**Pasta \\ shellex \\ PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="7ad41-139">**Folder\\shellex\\PropertySheetHandlers**</span></span>  
<span data-ttu-id="7ad41-140">**Componentes do instalador \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-140">**Installer\\Components**</span></span>  
<span data-ttu-id="7ad41-141">**Recursos do instalador \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-141">**Installer\\Features**</span></span>  
<span data-ttu-id="7ad41-142">**Produtos do instalador \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-142">**Installer\\Products**</span></span>  
<span data-ttu-id="7ad41-143">**Interface**</span><span class="sxs-lookup"><span data-stu-id="7ad41-143">**Interface**</span></span>  
<span data-ttu-id="7ad41-144">**MIME**</span><span class="sxs-lookup"><span data-stu-id="7ad41-144">**Mime**</span></span>  
<span data-ttu-id="7ad41-145">**\\Banco de dados MIME**</span><span class="sxs-lookup"><span data-stu-id="7ad41-145">**Mime\\Database**</span></span>  
<span data-ttu-id="7ad41-146">**Conjunto de \\ caracteres de banco de dados MIME \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-146">**Mime\\Database\\Charset**</span></span>  
<span data-ttu-id="7ad41-147">**\\Página de código do banco de dados MIME \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-147">**Mime\\Database\\Codepage**</span></span>  
<span data-ttu-id="7ad41-148">**\\Tipo de conteúdo do banco de dados MIME \\**</span><span class="sxs-lookup"><span data-stu-id="7ad41-148">**Mime\\Database\\Content Type**</span></span>  
<span data-ttu-id="7ad41-149">**Importação**</span><span class="sxs-lookup"><span data-stu-id="7ad41-149">**Typelib**</span></span>  


 

 
