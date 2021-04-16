---
description: Você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalando um componente ausente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752248"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="9d98c-103">Instalando um componente ausente</span><span class="sxs-lookup"><span data-stu-id="9d98c-103">Installing a Missing Component</span></span>

<span data-ttu-id="9d98c-104">Você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="9d98c-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="9d98c-105">Como o instalador instala recursos e não componentes, ele deve primeiro resolver a qual componente um arquivo ausente pertence e, em seguida, instalar o recurso que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="9d98c-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="9d98c-106">Se mais de um recurso estiver vinculado ao componente, o instalador instalará o recurso que requer o menor espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="9d98c-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="9d98c-107">Se você chamar [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), poderá verificar se o arquivo de chave de um componente está presente.</span><span class="sxs-lookup"><span data-stu-id="9d98c-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="9d98c-108">No entanto, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes.</span><span class="sxs-lookup"><span data-stu-id="9d98c-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="9d98c-109">Nesse cenário, chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="9d98c-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="9d98c-110">O instalador, em seguida, resolve para qual componente o arquivo pertence e instala o recurso que está vinculado ao componente que requer o menor espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="9d98c-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="9d98c-111">Se a função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) falhar inesperadamente, você deverá instalar os componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="9d98c-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="9d98c-112">O procedimento a seguir mostra como instalar componentes ausentes.</span><span class="sxs-lookup"><span data-stu-id="9d98c-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="9d98c-113">**Para detectar e instalar um componente ausente**</span><span class="sxs-lookup"><span data-stu-id="9d98c-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="9d98c-114">Chame [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para verificar se o arquivo de chave de um componente está presente.</span><span class="sxs-lookup"><span data-stu-id="9d98c-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="9d98c-115">No entanto, mesmo que o arquivo de chave do componente esteja presente, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes.</span><span class="sxs-lookup"><span data-stu-id="9d98c-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="9d98c-116">Chame a função [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se o recurso associado ao componente for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9d98c-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="9d98c-117">Chame a função [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) ou [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se o recurso associado ao componente for conhecido.</span><span class="sxs-lookup"><span data-stu-id="9d98c-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="9d98c-118">Chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se um aplicativo não puder abrir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9d98c-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



