---
title: Gravando em um arquivo
description: Gravando em um arquivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Função AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757770"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="518cb-104">Gravando em um arquivo</span><span class="sxs-lookup"><span data-stu-id="518cb-104">Writing to a File</span></span>

<span data-ttu-id="518cb-105">Você pode gravar informações suplementares em um arquivo que foi aberto com privilégios de gravação usando a função [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) .</span><span class="sxs-lookup"><span data-stu-id="518cb-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="518cb-106">Essa função copia as informações de um buffer fornecido pelo aplicativo e a coloca em uma ou mais partes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="518cb-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="518cb-107">O bloco "INFO" é um tipo de parte de RIFF comum no qual a função armazena informações complementares.</span><span class="sxs-lookup"><span data-stu-id="518cb-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="518cb-108">Para obter uma descrição dos arquivos RIFF e de suas partes de dados, consulte [serviços de formato de arquivo de intercâmbio de recursos](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="518cb-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




