---
description: Demonstra como registrar um verbo que estende o &\# 0034; Sincronizar&\# 0034; e &\# 0034; Compartilhe&\# 0034; verbos na barra de comandos do Windows Explorer.
title: Sincronizar e compartilhar verbos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968200"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="359b8-103">Sincronizar e compartilhar verbos</span><span class="sxs-lookup"><span data-stu-id="359b8-103">Sync and Share Verbs</span></span>

<span data-ttu-id="359b8-104">Demonstra como registrar um verbo que estende os verbos de "sincronização" e "compartilhamento" na barra de comandos do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="359b8-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="359b8-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="359b8-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="359b8-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="359b8-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="359b8-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="359b8-108">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="359b8-109">Removendo o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="359b8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="359b8-110">Requirements</span></span>



| <span data-ttu-id="359b8-111">Produto</span><span class="sxs-lookup"><span data-stu-id="359b8-111">Product</span></span>                                | <span data-ttu-id="359b8-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="359b8-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="359b8-113">Windows</span><span class="sxs-lookup"><span data-stu-id="359b8-113">Windows</span></span>                                | <span data-ttu-id="359b8-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="359b8-114">Windows 7</span></span>               |
| <span data-ttu-id="359b8-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="359b8-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="359b8-116">7.0</span><span class="sxs-lookup"><span data-stu-id="359b8-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="359b8-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-117">Downloading the Sample</span></span>

| <span data-ttu-id="359b8-118">Localização</span><span class="sxs-lookup"><span data-stu-id="359b8-118">Location</span></span>      | <span data-ttu-id="359b8-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="359b8-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="359b8-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="359b8-120">GitHub</span></span>  | [<span data-ttu-id="359b8-121">Exemplo de SyncAndShareVerbs</span><span class="sxs-lookup"><span data-stu-id="359b8-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="359b8-122">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-122">Running the Sample</span></span>

<span data-ttu-id="359b8-123">Para executar o exemplo (sincronização):</span><span class="sxs-lookup"><span data-stu-id="359b8-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="359b8-124">Navegue até o diretório que contém o `sync.reg` arquivo</span><span class="sxs-lookup"><span data-stu-id="359b8-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="359b8-125">Digite `sync.reg ` na linha de comando ou clique duas vezes no ícone para `sync.reg` registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="359b8-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="359b8-126">Abra o Windows Explorer e selecione um arquivo.</span><span class="sxs-lookup"><span data-stu-id="359b8-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="359b8-127">Clique na opção **sincronizar** na barra de comandos e selecione uma subopção, como **Paint**.</span><span class="sxs-lookup"><span data-stu-id="359b8-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="359b8-128">Para executar o exemplo (compartilhamento):</span><span class="sxs-lookup"><span data-stu-id="359b8-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="359b8-129">Navegue até o diretório que contém o `share.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="359b8-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="359b8-130">Digite `share.reg` na linha de comando ou clique duas vezes no ícone para `share.reg` registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="359b8-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="359b8-131">Abra o Windows Explorer e selecione um arquivo.</span><span class="sxs-lookup"><span data-stu-id="359b8-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="359b8-132">Clique na opção **compartilhar** na barra de comandos.</span><span class="sxs-lookup"><span data-stu-id="359b8-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="359b8-133">Clique na opção **compartilhar com** na barra de comandos e selecione uma subopção, como o **Paint**.</span><span class="sxs-lookup"><span data-stu-id="359b8-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="359b8-134">Removendo o exemplo</span><span class="sxs-lookup"><span data-stu-id="359b8-134">Removing the Sample</span></span>

<span data-ttu-id="359b8-135">Para remover o exemplo (sincronização):</span><span class="sxs-lookup"><span data-stu-id="359b8-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="359b8-136">Navegue até o diretório que contém o arquivo Uninstallsync. reg.</span><span class="sxs-lookup"><span data-stu-id="359b8-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="359b8-137">Digite `uninstallsync.reg` na linha de comando ou clique duas vezes no ícone para `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="359b8-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="359b8-138">Para remover o exemplo (compartilhamento):</span><span class="sxs-lookup"><span data-stu-id="359b8-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="359b8-139">Navegue até o diretório que contém o arquivo Uninstallshare. reg.</span><span class="sxs-lookup"><span data-stu-id="359b8-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="359b8-140">Digite `uninstallshare.reg` na linha de comando ou clique duas vezes no ícone para `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="359b8-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



