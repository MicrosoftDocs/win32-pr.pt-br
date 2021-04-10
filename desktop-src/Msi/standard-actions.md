---
description: Uma ação encapsula uma função típica executada durante a instalação ou manutenção de um aplicativo. Windows Installer tem muitas ações internas padrão. Os desenvolvedores de pacotes de instalação também podem criar suas próprias ações personalizadas.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Ações padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165439"
---
# <a name="standard-actions"></a><span data-ttu-id="44450-105">Ações padrão</span><span class="sxs-lookup"><span data-stu-id="44450-105">Standard Actions</span></span>

<span data-ttu-id="44450-106">Uma ação encapsula uma função típica executada durante a instalação ou manutenção de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44450-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="44450-107">Windows Installer tem muitas ações internas padrão.</span><span class="sxs-lookup"><span data-stu-id="44450-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="44450-108">Os desenvolvedores de pacotes de instalação também podem criar suas próprias [ações personalizadas](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="44450-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="44450-109">Exemplos de ações padrão do instalador incluem:</span><span class="sxs-lookup"><span data-stu-id="44450-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="44450-110">[Ação Createatalhos](createshortcuts-action.md): gerencia a criação de atalhos para arquivos instalados com o aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="44450-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="44450-111">Essa ação usa a [tabela de atalho](shortcut-table.md) para seus dados.</span><span class="sxs-lookup"><span data-stu-id="44450-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="44450-112">[Ação InstallFiles](installfiles-action.md): copia os arquivos selecionados do diretório de origem para o diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="44450-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="44450-113">Essa ação usa a [tabela de arquivos](file-table.md) para seus dados.</span><span class="sxs-lookup"><span data-stu-id="44450-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="44450-114">[Ação WriteRegistryValues](writeregistryvalues-action.md): configura as informações do registro que o aplicativo requer no registro.</span><span class="sxs-lookup"><span data-stu-id="44450-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="44450-115">Essa ação usa a [tabela de registro](registry-table.md) para seus dados.</span><span class="sxs-lookup"><span data-stu-id="44450-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="44450-116">As seções a seguir discutem ações padrão.</span><span class="sxs-lookup"><span data-stu-id="44450-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="44450-117">Sobre as ações padrão</span><span class="sxs-lookup"><span data-stu-id="44450-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="44450-118">Usando ações padrão</span><span class="sxs-lookup"><span data-stu-id="44450-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="44450-119">Referência de ações padrão</span><span class="sxs-lookup"><span data-stu-id="44450-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



