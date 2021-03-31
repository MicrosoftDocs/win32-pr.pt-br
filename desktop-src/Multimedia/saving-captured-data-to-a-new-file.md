---
title: Salvando dados capturados em um novo arquivo
description: Salvando dados capturados em um novo arquivo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS mensagem
- macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635885"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="f8174-105">Salvando dados capturados em um novo arquivo</span><span class="sxs-lookup"><span data-stu-id="f8174-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="f8174-106">Se o usuário quiser salvar os dados capturados, o aplicativo deverá salvar o conteúdo do arquivo de captura em outro arquivo usando a [**mensagem \_ \_ \_ SaveAs do arquivo do WM Cap**](wm-cap-file-saveas.md) (ou a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ).</span><span class="sxs-lookup"><span data-stu-id="f8174-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="f8174-107">Essa mensagem não altera o nome ou o conteúdo do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="f8174-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="f8174-108">Seu aplicativo deve especificar um nome para o novo arquivo porque o arquivo de captura retém seu nome de arquivo original.</span><span class="sxs-lookup"><span data-stu-id="f8174-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="f8174-109">Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="f8174-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="f8174-110">Essa mensagem copia apenas a parte do arquivo de captura que contém os dados de captura.</span><span class="sxs-lookup"><span data-stu-id="f8174-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




