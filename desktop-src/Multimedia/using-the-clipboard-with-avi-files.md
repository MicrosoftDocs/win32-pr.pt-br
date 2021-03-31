---
title: Usando a área de transferência com arquivos AVI
description: Usando a área de transferência com arquivos AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Função AVIPutFileOnClipboard
- Função AVIGetFromClipboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635942"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="35d39-105">Usando a área de transferência com arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="35d39-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="35d39-106">A área de transferência fornece armazenamento temporário conveniente que um aplicativo pode usar para copiar ou transferir arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="35d39-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="35d39-107">O AVIFile inclui funções de área de transferência que você pode usar com arquivos de disco ou memória.</span><span class="sxs-lookup"><span data-stu-id="35d39-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="35d39-108">Você pode copiar um arquivo para a área de transferência usando a função [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) .</span><span class="sxs-lookup"><span data-stu-id="35d39-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="35d39-109">Para gravar um arquivo que está na área de transferência na memória ou no disco, use a função [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .</span><span class="sxs-lookup"><span data-stu-id="35d39-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="35d39-110">Você pode limpar um arquivo da área de transferência usando a função [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) .</span><span class="sxs-lookup"><span data-stu-id="35d39-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="35d39-111">Essa função não limpa outros tipos de informações, como texto, da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="35d39-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="35d39-112">Se você usar funções da área de transferência em seu aplicativo, desmarque a área de transferência com **AVIClearClipboard** antes de fechar o aplicativo ou fechar o arquivo na área de transferência.</span><span class="sxs-lookup"><span data-stu-id="35d39-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="35d39-113">Você pode chamar **AVIClearClipboard** em seu aplicativo se o **AVIPutFileOnClipboard** foi ou não usado.</span><span class="sxs-lookup"><span data-stu-id="35d39-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="35d39-114">Se o seu aplicativo copia um arquivo para a área de transferência e o arquivo contém dados de fluxo que podem ser alterados, você pode criar um arquivo de memória de fluxos clonados usando a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="35d39-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="35d39-115">Em seguida, você pode inserir o arquivo na área de transferência e liberar o arquivo original sem invalidar-o.</span><span class="sxs-lookup"><span data-stu-id="35d39-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




