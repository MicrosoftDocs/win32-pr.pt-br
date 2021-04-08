---
description: O Msizap.exe é um utilitário de linha de comando que remove todas as informações de Windows Installer de um produto ou de todos os produtos instalados em um computador. Os produtos instalados pelo instalador podem falhar ao funcionar depois de usar o Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010832"
---
# <a name="msizapexe"></a><span data-ttu-id="9d315-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="9d315-104">Msizap.exe</span></span>

<span data-ttu-id="9d315-105">O Msizap.exe é um utilitário de linha de comando que remove todas as informações de Windows Installer de um produto ou de todos os produtos instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="9d315-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="9d315-106">Os produtos instalados pelo instalador podem falhar ao funcionar depois de usar o Msizap.</span><span class="sxs-lookup"><span data-stu-id="9d315-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="9d315-107">No Windows 2000 e no Windows XP, são necessários privilégios administrativos para usar Msizap.exe.</span><span class="sxs-lookup"><span data-stu-id="9d315-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="9d315-108">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md) e não deve ser redistribuída.</span><span class="sxs-lookup"><span data-stu-id="9d315-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="9d315-109">Use a versão recente do Msizap.exe (versão 3.1.4000.2726 ou superior) que está disponível na SDK do Windows componentes para Windows Installer desenvolvedores para Windows Vista ou superior.</span><span class="sxs-lookup"><span data-stu-id="9d315-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="9d315-110">Versões menores do Msizap.exe podem remover informações sobre todas as atualizações que foram aplicadas a outros aplicativos no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="9d315-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="9d315-111">Se essas informações forem removidas, talvez esses outros aplicativos precisem ser removidos e reinstalados para receber atualizações adicionais.</span><span class="sxs-lookup"><span data-stu-id="9d315-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d315-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d315-112">Syntax</span></span>

<span data-ttu-id="9d315-113">**Msizap T**_\[ wa! \] {código do produto}_</span><span class="sxs-lookup"><span data-stu-id="9d315-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="9d315-114">**Msizap T**_\[ wa! \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="9d315-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="9d315-115">\**\* \*\*\* Msizap \[ WA! \]* **Produtos**</span><span class="sxs-lookup"><span data-stu-id="9d315-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="9d315-116">**Msizap PWSA?!**</span><span class="sxs-lookup"><span data-stu-id="9d315-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="9d315-117">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="9d315-117">Command Line Options</span></span>

<span data-ttu-id="9d315-118">Msizap.exe usa opções de linha de comando que não diferenciam maiúsculas de minúsculas mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d315-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="9d315-119">Opção</span><span class="sxs-lookup"><span data-stu-id="9d315-119">Option</span></span> | <span data-ttu-id="9d315-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d315-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="9d315-121">Remove todas as pastas de Windows Installer e chaves do registro, ajusta as contagens de DLL compartilhadas e interrompe Windows Installer serviço.</span><span class="sxs-lookup"><span data-stu-id="9d315-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="9d315-122">Também remove a chave In-Progress e informações de reversão.</span><span class="sxs-lookup"><span data-stu-id="9d315-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="9d315-123">um</span><span class="sxs-lookup"><span data-stu-id="9d315-123">a</span></span>      | <span data-ttu-id="9d315-124">Só altera ACLs para controle total de administrador para qualquer remoção especificada.</span><span class="sxs-lookup"><span data-stu-id="9d315-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="9d315-125">g</span><span class="sxs-lookup"><span data-stu-id="9d315-125">g</span></span>      | <span data-ttu-id="9d315-126">Para todos os usuários, o Remove todos os arquivos de dados de Windows Installer em cache que ficaram órfãos.</span><span class="sxs-lookup"><span data-stu-id="9d315-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9d315-127">p</span><span class="sxs-lookup"><span data-stu-id="9d315-127">p</span></span>      | <span data-ttu-id="9d315-128">Remove a chave de In-Progress.</span><span class="sxs-lookup"><span data-stu-id="9d315-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="9d315-129">s</span><span class="sxs-lookup"><span data-stu-id="9d315-129">s</span></span>      | <span data-ttu-id="9d315-130">Remove informações de reversão.</span><span class="sxs-lookup"><span data-stu-id="9d315-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d315-131">t</span><span class="sxs-lookup"><span data-stu-id="9d315-131">t</span></span>      | <span data-ttu-id="9d315-132">Remove todas as informações do código de produto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d315-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="9d315-133">Ao usar essa opção, coloque o código do produto entre chaves.</span><span class="sxs-lookup"><span data-stu-id="9d315-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="9d315-134">Essa opção pode ser usada com o caminho completo para o arquivo. msi ou com o código do produto.</span><span class="sxs-lookup"><span data-stu-id="9d315-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="9d315-135">w</span><span class="sxs-lookup"><span data-stu-id="9d315-135">w</span></span>      | <span data-ttu-id="9d315-136">Remove informações de Windows Installer para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="9d315-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="9d315-137">Quando essa opção não é definida, somente as informações do usuário atual são removidas.</span><span class="sxs-lookup"><span data-stu-id="9d315-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="9d315-138">O uso dessa opção requer que o perfil do usuário seja carregado para que o hive do registro por usuário do usuário esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="9d315-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="9d315-139">?</span><span class="sxs-lookup"><span data-stu-id="9d315-139">?</span></span>      | <span data-ttu-id="9d315-140">Ajuda detalhada.</span><span class="sxs-lookup"><span data-stu-id="9d315-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9d315-141">!</span><span class="sxs-lookup"><span data-stu-id="9d315-141">!</span></span>      | <span data-ttu-id="9d315-142">Força uma resposta ' Sim ' a qualquer prompt.</span><span class="sxs-lookup"><span data-stu-id="9d315-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9d315-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d315-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d315-144">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="9d315-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



