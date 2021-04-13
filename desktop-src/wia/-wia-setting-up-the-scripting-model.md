---
description: Para usar o modelo de script da aquisição de imagens do Windows (WIA), você deve ter o arquivo Wiascr.dll instalado e registrado no computador.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurando o ambiente de desenvolvimento do modelo de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164524"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="e8dea-103">Configurando o ambiente de desenvolvimento do modelo de script</span><span class="sxs-lookup"><span data-stu-id="e8dea-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="e8dea-104">Para usar o modelo de script da aquisição de imagens do Windows (WIA), você deve ter o arquivo Wiascr.dll instalado e registrado no computador.</span><span class="sxs-lookup"><span data-stu-id="e8dea-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="e8dea-105">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="e8dea-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="e8dea-106">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="e8dea-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="e8dea-107">Copie esse arquivo do SDK do WIA para o diretório *% windir%*/system32 (por exemplo, c \\ : \\ Windows system32).</span><span class="sxs-lookup"><span data-stu-id="e8dea-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="e8dea-108">Na linha de comando, navegue até esse diretório e digite **regsvr32 Wiascr.dll**.</span><span class="sxs-lookup"><span data-stu-id="e8dea-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="e8dea-109">Isso insere as informações necessárias no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="e8dea-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="e8dea-110">Agora você está pronto para usar o modelo de script WIA.</span><span class="sxs-lookup"><span data-stu-id="e8dea-110">You are now ready to use the WIA scripting model.</span></span>

 

 
