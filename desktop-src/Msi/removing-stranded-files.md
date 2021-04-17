---
description: Uma lista de possíveis motivos pelos quais uma desinstalação do Windows Installer não pôde remover todos os arquivos de um aplicativo.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Removendo arquivos perdidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787495"
---
# <a name="removing-stranded-files"></a><span data-ttu-id="ac2f1-103">Removendo arquivos perdidos</span><span class="sxs-lookup"><span data-stu-id="ac2f1-103">Removing Stranded Files</span></span>

<span data-ttu-id="ac2f1-104">Se um arquivo que deveria ter sido removido do computador do usuário permanecer instalado após a execução de uma desinstalação, talvez o instalador não esteja removendo o componente que contém o arquivo por um ou mais dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="ac2f1-104">If a file that should have been removed from the user's computer remains installed after running an uninstall, the installer may not be removing the component containing the file for one or more of the following reasons:</span></span>

-   <span data-ttu-id="ac2f1-105">O bit msidbComponentAttributesPermanent foi definido para o componente na coluna Attributes da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-105">The msidbComponentAttributesPermanent bit was set for the component in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="ac2f1-106">Nenhum valor foi inserido para o componente na coluna ComponentID da tabela Component.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-106">No value was entered for the component in the ComponentId column of the Component table.</span></span>
-   <span data-ttu-id="ac2f1-107">O componente é usado por outro aplicativo ou recurso que ainda está instalado.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-107">The component is used by another application or feature that is still installed.</span></span>
-   <span data-ttu-id="ac2f1-108">Há uma condição especificada na tabela de [condição](condition-table.md) que habilita um recurso durante a instalação e desabilita o recurso durante a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-108">There is a condition specified in the [Condition](condition-table.md) table that enables a feature during installation and disables the feature during uninstallation.</span></span>
-   <span data-ttu-id="ac2f1-109">O arquivo de chave para o componente tem uma contagem de referência anterior em **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-109">The key file for the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="ac2f1-110">O componente é instalado na pasta System e qualquer arquivo no componente tem uma contagem de referência anterior em **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-110">The component is installed in the System folder and any file in the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="ac2f1-111">O Windows Installer não remove nenhum arquivo ou chave do Registro protegido por [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) (WRP).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-111">The Windows Installer does not remove any files or registry keys that are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP).</span></span> <span data-ttu-id="ac2f1-112">Para obter mais informações, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-112">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span> <span data-ttu-id="ac2f1-113">No Windows Server 2003, Windows XP e Windows 2000, o instalador não remove nenhum arquivo protegido pela WFP (proteção de arquivo do Windows).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-113">On Windows Server 2003, Windows XP, and Windows 2000, the installer does not remove any files that are protected by Windows File Protection (WFP).</span></span> <span data-ttu-id="ac2f1-114">Se o arquivo de caminho de chave do componente ou a chave do registro for protegido por WFP ou WRP, o instalador não removerá o componente.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-114">If a component's key path file or registry key is protected by WFP or WRP, the installer does not remove the component.</span></span>
    > [!Note]  
    > <span data-ttu-id="ac2f1-115">Como Windows Installer não instala, atualiza ou remove qualquer recurso protegido por WRP, você não deve incluir recursos protegidos em um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-115">Because Windows Installer does not install, update, or remove any resource that is protected by WRP, you should not include protected resources in an installation package.</span></span> <span data-ttu-id="ac2f1-116">Em vez disso, use apenas os [mecanismos de substituição de recursos com suporte](../wfp/supported-file-replacement-mechanisms.md) descritos na seção [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2f1-116">Instead, use only the [supported resource replacement mechanisms](../wfp/supported-file-replacement-mechanisms.md) described in the [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) section.</span></span>

     

 

 
