---
description: Para adicionar um item ao submenu programas, siga estas etapas.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Como adicionar atalhos ao menu iniciar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091611"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="41cfd-103">Como adicionar atalhos ao menu iniciar</span><span class="sxs-lookup"><span data-stu-id="41cfd-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="41cfd-104">Para adicionar um item ao submenu **programas** , siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="41cfd-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="41cfd-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="41cfd-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="41cfd-106">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="41cfd-106">Step 1:</span></span>

<span data-ttu-id="41cfd-107">Crie um [link do Shell](./links.md) usando a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="41cfd-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="41cfd-108">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="41cfd-108">Step 2:</span></span>

<span data-ttu-id="41cfd-109">Obtenha o local da pasta programas usando a função [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , passando os [**\_ programas FolderId**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="41cfd-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="41cfd-110">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="41cfd-110">Step 3:</span></span>

<span data-ttu-id="41cfd-111">Adicione o link do Shell à pasta programas.</span><span class="sxs-lookup"><span data-stu-id="41cfd-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="41cfd-112">Você também pode criar uma pasta na pasta programas e adicionar o link a essa pasta.</span><span class="sxs-lookup"><span data-stu-id="41cfd-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
