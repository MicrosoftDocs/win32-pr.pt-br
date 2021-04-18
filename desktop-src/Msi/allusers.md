---
Description: A propriedade ALLUSERS configura o contexto de instalação do pacote.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Propriedade ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778736"
---
# <a name="allusers-property"></a><span data-ttu-id="41678-103">Propriedade ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="41678-103">ALLUSERS property</span></span>

<span data-ttu-id="41678-104">A propriedade **AllUsers** configura o contexto de instalação do pacote.</span><span class="sxs-lookup"><span data-stu-id="41678-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="41678-105">O Windows Installer executa uma instalação por usuário ou instalação por máquina, dependendo dos privilégios de acesso do usuário, se forem necessários privilégios elevados para instalar o aplicativo, o valor da propriedade **AllUsers** , o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) e a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41678-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="41678-106">O valor da propriedade **AllUsers** , no momento da instalação, determina o [contexto de instalação](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="41678-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="41678-107">Um valor de propriedade **AllUsers** de 1 especifica o contexto de instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="41678-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="41678-108">Um valor de propriedade **AllUsers** de uma cadeia de caracteres vazia ("") especifica o contexto de instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="41678-109">Se o valor da propriedade **AllUsers** for definido como 2, o Windows Installer sempre redefinirá o valor da propriedade **AllUsers** como 1 e executará uma instalação por computador ou redefinirá o valor da propriedade **AllUsers** como uma cadeia de caracteres vazia ("") e executará uma instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="41678-110">O valor ALLUSERS = 2 permite que o sistema redefina o valor de **AllUsers** e o contexto de instalação, dependendo dos privilégios do usuário e da versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="41678-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="41678-111">**Windows 7:** Defina a propriedade **AllUsers** como 2 para usar a propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) para especificar o contexto de instalação.</span><span class="sxs-lookup"><span data-stu-id="41678-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="41678-112">Defina a propriedade **MSIINSTALLPERUSER** como uma cadeia de caracteres vazia ("") para uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="41678-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="41678-113">Defina a propriedade **MSIINSTALLPERUSER** como 1 para uma instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="41678-114">Se o pacote tiver sido escrito seguindo as diretrizes de desenvolvimento descritas em [criação de pacote único](single-package-authoring.md), os usuários que tiverem acesso de usuário poderão instalar no contexto por usuário sem precisar fornecer credenciais do UAC.</span><span class="sxs-lookup"><span data-stu-id="41678-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="41678-115">Se o usuário tiver privilégios de acesso de usuário, o instalador executará uma instalação por máquina somente se as credenciais de administrador forem fornecidas para a caixa de diálogo do UAC.</span><span class="sxs-lookup"><span data-stu-id="41678-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="41678-116">**Windows Vista:** Defina a propriedade **AllUsers** como 2 e Windows Installer está em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="41678-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="41678-117">Se o usuário tiver privilégios de acesso de usuário e ALLUSERS = 2, o instalador executará uma instalação por máquina somente se as credenciais de administrador forem fornecidas para a caixa de diálogo do UAC.</span><span class="sxs-lookup"><span data-stu-id="41678-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="41678-118">Se o UAC estiver habilitado e as credenciais de administrador corretas não forem fornecidas, a instalação falhará com um erro informando que privilégios de administrador são necessários.</span><span class="sxs-lookup"><span data-stu-id="41678-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="41678-119">Se o UAC for desabilitado pela chave do registro, pela política de grupo ou pelo painel de controle, a caixa de diálogo UAC não será exibida e a instalação falhará com um erro informando que privilégios de administrador são necessários.</span><span class="sxs-lookup"><span data-stu-id="41678-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="41678-120">**Windows XP:** Defina a propriedade **AllUsers** como 2 e Windows Installer executará uma instalação por usuário se o usuário tiver privilégios de acesso de usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="41678-121">Se o valor da propriedade **AllUsers** não for igual a 2, o Windows Installer ignorará o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) .</span><span class="sxs-lookup"><span data-stu-id="41678-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="41678-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="41678-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="41678-123">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) no github.</span><span class="sxs-lookup"><span data-stu-id="41678-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="41678-124">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="41678-124">Default Value</span></span>

<span data-ttu-id="41678-125">O contexto de instalação padrão recomendado é por usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="41678-126">Se **AllUsers** não estiver definido, o instalador fará uma instalação por usuário.</span><span class="sxs-lookup"><span data-stu-id="41678-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="41678-127">Você pode garantir que a propriedade **AllUsers** não tenha sido definida definindo seu valor como uma cadeia de caracteres vazia (""), ALLUSERS = "".</span><span class="sxs-lookup"><span data-stu-id="41678-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="41678-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="41678-128">Remarks</span></span>

<span data-ttu-id="41678-129">O [contexto de instalação](installation-context.md) determina os valores das propriedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="41678-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="41678-130">O contexto de instalação determina as partes do registro em que as entradas na [tabela de registro](registry-table.md) e na [tabela RemoveRegistry](removeregistry-table.md), com-1 na coluna raiz, são gravadas ou removidas.</span><span class="sxs-lookup"><span data-stu-id="41678-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="41678-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41678-131">Requirements</span></span>



| <span data-ttu-id="41678-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="41678-132">Requirement</span></span> | <span data-ttu-id="41678-133">Valor</span><span class="sxs-lookup"><span data-stu-id="41678-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41678-134">Versão</span><span class="sxs-lookup"><span data-stu-id="41678-134">Version</span></span><br/> | <span data-ttu-id="41678-135">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41678-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="41678-136">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="41678-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="41678-137">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41678-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="41678-138">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="41678-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41678-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="41678-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41678-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41678-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="41678-141">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="41678-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="41678-142">Contexto de instalação</span><span class="sxs-lookup"><span data-stu-id="41678-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="41678-143">Criação de pacote único</span><span class="sxs-lookup"><span data-stu-id="41678-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




