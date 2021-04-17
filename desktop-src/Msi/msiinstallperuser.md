---
description: As propriedades MSIINSTALLPERUSER e ALLUSERS podem ser definidas pelo usuário no momento da instalação, por meio da interface do usuário ou em uma linha de comando, para solicitar que o Windows Installer instale um pacote de uso duplo para o usuário atual ou todos os usuários do computador.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propriedade MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752638"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="3a411-103">Propriedade MSIINSTALLPERUSER</span><span class="sxs-lookup"><span data-stu-id="3a411-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="3a411-104">As propriedades **MSIINSTALLPERUSER** e [**AllUsers**](allusers.md) podem ser definidas pelo usuário no momento da instalação, por meio da interface do usuário ou em uma linha de comando, para solicitar que o Windows Installer instale um pacote de uso duplo para o usuário atual ou todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="3a411-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="3a411-105">Para usar a propriedade **MSIINSTALLPERUSER** , o valor da propriedade [**AllUsers**](allusers.md) deve ser 2 e o pacote precisa ter sido criado para ser capaz de ser instalado no contexto por usuário ou por máquina.</span><span class="sxs-lookup"><span data-stu-id="3a411-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="3a411-106">Para obter informações sobre como criar um pacote de uso duplo, consulte [criação de pacote único](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="3a411-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="3a411-107">Se o valor da propriedade **AllUsers** não for igual a 2, o valor da propriedade **MSIINSTALLPERUSER** será ignorado e não terá efeito sobre a instalação.</span><span class="sxs-lookup"><span data-stu-id="3a411-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="3a411-108">O valor da propriedade **MSIINSTALLPERUSER** é ignorado ao instalar o pacote usando Windows Installer 4,5 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="3a411-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="3a411-109">Para solicitar que o Windows Installer instale o pacote de uso duplo no [contexto de instalação](installation-context.md)por máquina, o usuário pode definir o valor da propriedade **MSIINSTALLPERUSER** como uma cadeia de caracteres vazia ("") e o valor da propriedade [**AllUsers**](allusers.md) como 2 usando uma interface de usuário criada ou uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3a411-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="3a411-110">Para solicitar que o Windows Installer instale o pacote de uso duplo no [contexto de instalação](installation-context.md)por usuário, o usuário pode definir o valor da propriedade **MSIINSTALLPERUSER** como 1 e o valor da propriedade [**AllUsers**](allusers.md) como 2 usando uma interface de usuário criada ou uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3a411-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="3a411-111">Se o valor da propriedade [**AllUsers**](allusers.md) não for igual a 2, o Windows Installer ignorará o valor da propriedade **MSIINSTALLPERUSER** .</span><span class="sxs-lookup"><span data-stu-id="3a411-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="3a411-112">Se Windows Installer instalar o aplicativo no contexto por máquina, ele redefinirá o valor da propriedade **AllUsers** como 1.</span><span class="sxs-lookup"><span data-stu-id="3a411-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="3a411-113">Se Windows Installer instalar o aplicativo no contexto por usuário, ele redefinirá o valor da propriedade **AllUsers** como uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="3a411-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="3a411-114">Os aplicativos que foram instalados por usuário, portanto, recebem todas as atualizações ou reparos em uma base por usuário e aplicativos instalados por computador recebem atualizações ou reparos em uma base por máquina.</span><span class="sxs-lookup"><span data-stu-id="3a411-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="3a411-115">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** a propriedade **MSIINSTALLPERUSER** é ignorada pelas versões anteriores à Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a411-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="3a411-116">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="3a411-116">Default Value</span></span>

<span data-ttu-id="3a411-117">O contexto de instalação padrão recomendado é por usuário para um pacote de uso duplo.</span><span class="sxs-lookup"><span data-stu-id="3a411-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="3a411-118">Autor MSIINSTALLPERUSER = 1 e ALLUSERS = 2 na [tabela de propriedades](property-table.md) do pacote de uso duplo para especificar por usuário como o contexto de instalação padrão.</span><span class="sxs-lookup"><span data-stu-id="3a411-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a411-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a411-119">Remarks</span></span>

<span data-ttu-id="3a411-120">Você pode garantir que a propriedade **MSIINSTALLPERUSER** não tenha sido definida definindo seu valor como uma cadeia de caracteres vazia (""), MSIINSTALLPERUSER = "".</span><span class="sxs-lookup"><span data-stu-id="3a411-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="3a411-121">O contexto de instalação determina os valores das propriedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="3a411-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="3a411-122">O contexto de instalação determina as partes do registro em que as entradas na [tabela de registro](registry-table.md) e na [tabela RemoveRegistry](removeregistry-table.md), com-1 na coluna raiz, são gravadas ou removidas.</span><span class="sxs-lookup"><span data-stu-id="3a411-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="3a411-123">Para obter informações sobre o contexto de instalação, consulte [contexto de instalação](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="3a411-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a411-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a411-124">Requirements</span></span>



| <span data-ttu-id="3a411-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a411-125">Requirement</span></span> | <span data-ttu-id="3a411-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3a411-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a411-127">Versão</span><span class="sxs-lookup"><span data-stu-id="3a411-127">Version</span></span><br/> | <span data-ttu-id="3a411-128">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a411-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3a411-129">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3a411-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a411-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a411-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a411-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a411-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="3a411-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="3a411-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="3a411-133">Contexto de instalação</span><span class="sxs-lookup"><span data-stu-id="3a411-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="3a411-134">Criação de pacote único</span><span class="sxs-lookup"><span data-stu-id="3a411-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




