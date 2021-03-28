---
description: O Windows Vista apresenta novos cenários de armazenamento e um novo namespace de perfil de usuário.
title: Pastas conhecidas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968073"
---
# <a name="known-folders"></a><span data-ttu-id="09d67-103">Pastas conhecidas</span><span class="sxs-lookup"><span data-stu-id="09d67-103">Known Folders</span></span>

<span data-ttu-id="09d67-104">O Windows Vista apresenta novos cenários de armazenamento e um novo namespace de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="09d67-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="09d67-105">Para resolver esses novos fatores, o sistema mais antigo de se referir a pastas padrão por um valor de [**CSIDL**](csidl.md) foi substituído.</span><span class="sxs-lookup"><span data-stu-id="09d67-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="09d67-106">A partir do Windows Vista, essas pastas são referenciadas por um novo conjunto de valores GUID chamado IDs de pasta conhecidas.</span><span class="sxs-lookup"><span data-stu-id="09d67-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="09d67-107">O sistema de pastas conhecido fornece estas vantagens:</span><span class="sxs-lookup"><span data-stu-id="09d67-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="09d67-108">ISVs (fornecedores independentes de software) podem estender o conjunto de IDs de pasta conhecidas com suas próprias.</span><span class="sxs-lookup"><span data-stu-id="09d67-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="09d67-109">Eles podem definir pastas, fornecer IDs e registrá-las no sistema.</span><span class="sxs-lookup"><span data-stu-id="09d67-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="09d67-110">Não foi possível estender os valores CSIDl.</span><span class="sxs-lookup"><span data-stu-id="09d67-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="09d67-111">Todas as pastas conhecidas em um sistema podem ser enumeradas.</span><span class="sxs-lookup"><span data-stu-id="09d67-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="09d67-112">Nenhuma API forneceu essa funcionalidade para valores de CSIDl.</span><span class="sxs-lookup"><span data-stu-id="09d67-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="09d67-113">Consulte [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="09d67-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="09d67-114">Uma pasta conhecida adicionada por um ISV pode adicionar propriedades personalizadas que permitem que ele explique sua finalidade e uso pretendido.</span><span class="sxs-lookup"><span data-stu-id="09d67-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="09d67-115">Muitas pastas conhecidas podem ser redirecionadas para novos locais, incluindo locais de rede.</span><span class="sxs-lookup"><span data-stu-id="09d67-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="09d67-116">No sistema CSIDl, somente a pasta **meus documentos** poderia ser redirecionada.</span><span class="sxs-lookup"><span data-stu-id="09d67-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="09d67-117">As pastas conhecidas podem ter manipuladores personalizados para uso durante a criação ou exclusão.</span><span class="sxs-lookup"><span data-stu-id="09d67-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="09d67-118">O sistema CSIDl e as APIs que usam valores de CSIDl ainda têm suporte para compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="09d67-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="09d67-119">No entanto, não é recomendável usá-los em qualquer desenvolvimento novo.</span><span class="sxs-lookup"><span data-stu-id="09d67-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="09d67-120">Os tópicos a seguir discutem as especificidades do sistema de pastas conhecidas.</span><span class="sxs-lookup"><span data-stu-id="09d67-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="09d67-121">Trabalhando com pastas conhecidas em aplicativos</span><span class="sxs-lookup"><span data-stu-id="09d67-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="09d67-122">Como estender pastas conhecidas com pastas personalizadas</span><span class="sxs-lookup"><span data-stu-id="09d67-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="09d67-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="09d67-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="09d67-124">As páginas de referência a seguir explicam as funções de pastas conhecidas do Win32, que podem ser usadas para recuperar o local de pastas conhecidas ou redirecioná-las para um novo local.</span><span class="sxs-lookup"><span data-stu-id="09d67-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="09d67-125">Essas funções substituem as funções mais antigas do Win32.</span><span class="sxs-lookup"><span data-stu-id="09d67-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="09d67-126">As novas funções são fornecidas para dar um comportamento equivalente às funções antigas, mas cada nova função também é duplicada por uma API de Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="09d67-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="09d67-127">Nova função</span><span class="sxs-lookup"><span data-stu-id="09d67-127">New Function</span></span>                                             | <span data-ttu-id="09d67-128">Substituto</span><span class="sxs-lookup"><span data-stu-id="09d67-128">Replaces</span></span>                                           | <span data-ttu-id="09d67-129">Equivalente COM</span><span class="sxs-lookup"><span data-stu-id="09d67-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="09d67-130">**SHGetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="09d67-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="09d67-132">**IKnownFolder:: GetPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="09d67-133">**SHGetKnownFolderIDList**</span><span class="sxs-lookup"><span data-stu-id="09d67-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="09d67-134">**SHGetFolderLocation**</span><span class="sxs-lookup"><span data-stu-id="09d67-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="09d67-135">**IKnownFolder::GetIDList**</span><span class="sxs-lookup"><span data-stu-id="09d67-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="09d67-136">**SHSetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="09d67-137">**SHSetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="09d67-138">**IKnownFolder:: SetPath**</span><span class="sxs-lookup"><span data-stu-id="09d67-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="09d67-139">As páginas de referência a seguir explicam as APIs de pastas conhecidas do COM, que fornecem toda a funcionalidade das APIs do Win32 listadas acima, além de adicionar a capacidade de enumerar todas as pastas conhecidas, acessar propriedades de pasta conhecidas e estender o conjunto padrão de pastas conhecidas.</span><span class="sxs-lookup"><span data-stu-id="09d67-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="09d67-140">**IKnownFolder**</span><span class="sxs-lookup"><span data-stu-id="09d67-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="09d67-141">**IKnownFolderManager**</span><span class="sxs-lookup"><span data-stu-id="09d67-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="09d67-142">Um exemplo de C++ que demonstra as APIs de pasta conhecidas está incluído no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="09d67-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09d67-143">Depois de instalar o SDK do Windows em seu computador, o exemplo poderá ser encontrado em% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ shell \\ AppPlatform \\ KnownFolders.</span><span class="sxs-lookup"><span data-stu-id="09d67-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09d67-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09d67-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="09d67-145">[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09d67-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
