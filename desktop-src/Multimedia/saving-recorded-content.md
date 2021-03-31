---
title: Salvando conteúdo gravado
description: Salvando conteúdo gravado
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Macro MCIWndSave
- Macro MCIWndSaveDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635884"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="e9ff6-105">Salvando conteúdo gravado</span><span class="sxs-lookup"><span data-stu-id="e9ff6-105">Saving Recorded Content</span></span>

<span data-ttu-id="e9ff6-106">Depois de concluir a gravação, você pode salvar o conteúdo usando a macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) ou [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) ou usando a função [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) com **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="e9ff6-107">A macro **MCIWndSave** salva os dados no arquivo associado à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="e9ff6-108">A macro **MCIWndSaveDialog** permite que o usuário especifique um nome de arquivo e salve os dados gravados no arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="e9ff6-109">A função **GetSaveFileNamePreview** exibe a caixa de diálogo **salvar** como para escolher um arquivo e permite que o usuário visualize (Execute) o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="e9ff6-110">Quando o nome de um arquivo existente é especificado na caixa de diálogo **salvar** como, o **GetSaveFileNamePreview** fornece um pequeno controle na caixa de diálogo para permitir que o usuário visualize o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="e9ff6-111">Você pode salvar os dados gravados em um arquivo selecionado com **GetSaveFileNamePreview** usando **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="e9ff6-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




