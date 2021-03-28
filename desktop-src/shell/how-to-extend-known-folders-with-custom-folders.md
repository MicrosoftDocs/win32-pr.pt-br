---
description: ISVs (fornecedores independentes de software) podem estender o conjunto de pastas conhecidas em um sistema registrando suas próprias pastas conhecidas.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Como estender pastas conhecidas com pastas personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169430"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="fca72-103">Como estender pastas conhecidas com pastas personalizadas</span><span class="sxs-lookup"><span data-stu-id="fca72-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="fca72-104">ISVs (fornecedores independentes de software) podem estender o conjunto de pastas conhecidas em um sistema registrando suas próprias pastas conhecidas.</span><span class="sxs-lookup"><span data-stu-id="fca72-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="fca72-105">Depois de registrado, essas pastas de terceiros são conhecidas pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="fca72-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="fca72-106">Eles são encontrados por qualquer chamada para [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span><span class="sxs-lookup"><span data-stu-id="fca72-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="fca72-107">Observe que uma pasta conhecida deve ser uma pasta por computador.</span><span class="sxs-lookup"><span data-stu-id="fca72-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="fca72-108">Não é possível criar uma pasta por usuário conhecida.</span><span class="sxs-lookup"><span data-stu-id="fca72-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="fca72-109">Instruções</span><span class="sxs-lookup"><span data-stu-id="fca72-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="fca72-110">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="fca72-110">Step 1:</span></span>

<span data-ttu-id="fca72-111">Defina sua pasta conhecida por meio de uma estrutura de [**\_ definição de KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .</span><span class="sxs-lookup"><span data-stu-id="fca72-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="fca72-112">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="fca72-112">Step 2:</span></span>

<span data-ttu-id="fca72-113">Registre a pasta conhecida por meio de uma chamada para [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span><span class="sxs-lookup"><span data-stu-id="fca72-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="fca72-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fca72-114">Remarks</span></span>

<span data-ttu-id="fca72-115">Se você criar uma pasta conhecida para seu aplicativo como parte do seu procedimento de instalação, também deverá incluir [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) como parte do seu código de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fca72-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="fca72-116">Considere por que você deseja que sua pasta seja incluída no sistema de pastas conhecido antes de registrá-la.</span><span class="sxs-lookup"><span data-stu-id="fca72-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="fca72-117">Você deve ter um motivo válido para elevar sua pasta para esse nível de visibilidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="fca72-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fca72-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fca72-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fca72-119">[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fca72-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
