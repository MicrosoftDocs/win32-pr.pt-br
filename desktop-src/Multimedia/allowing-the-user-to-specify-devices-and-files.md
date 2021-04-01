---
title: Permitindo que o usuário especifique dispositivos e arquivos
description: Permitindo que o usuário especifique dispositivos e arquivos
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Macro MCIWndOpenDialog
- Macro MCIWndOpen
- Macro MCIWndOpenInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636063"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="19190-106">Permitindo que o usuário especifique dispositivos e arquivos</span><span class="sxs-lookup"><span data-stu-id="19190-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="19190-107">Você pode associar um dispositivo ou arquivo a uma janela MCIWnd existente usando as macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)e [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) e a função [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="19190-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="19190-108">Para permitir que um usuário do seu aplicativo selecione um arquivo a ser reproduzido, use **MCIWndOpenDialog**.</span><span class="sxs-lookup"><span data-stu-id="19190-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="19190-109">Essa macro exibe a caixa de diálogo **abrir** (mostrada na captura de tela a seguir) para escolher um arquivo e associar o arquivo selecionado à janela MCIWnd atual.</span><span class="sxs-lookup"><span data-stu-id="19190-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![imagem da janela MCIWnd](images/mciwnd3.gif)

<span data-ttu-id="19190-111">Você pode permitir que um usuário do seu aplicativo selecione um arquivo a ser associado a uma janela do MCIWnd e visualize esse arquivo usando [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span><span class="sxs-lookup"><span data-stu-id="19190-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="19190-112">A função **GetOpenFileNamePreview** exibe a caixa de diálogo **abrir** para escolher um arquivo e permite que o usuário visualize (reproduza) seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19190-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="19190-113">Quando o nome de um arquivo existente é especificado na caixa de diálogo, **GetOpenFileNamePreview** fornece um pequeno controle para permitir que o usuário visualize o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="19190-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="19190-114">Você pode associar um arquivo especificado, selecionado com **GetOpenFileNamePreview** ou especificado de outra maneira, com uma janela MCIWnd usando **MCIWndOpen**.</span><span class="sxs-lookup"><span data-stu-id="19190-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="19190-115">Você também pode usar **MCIWndOpen** para especificar um dispositivo a ser associado a uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="19190-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="19190-116">Por exemplo, você pode usar um nome de dispositivo, como "CDAudio".</span><span class="sxs-lookup"><span data-stu-id="19190-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="19190-117">Para associar uma janela MCIWnd a uma interface de arquivo ou a uma interface de fluxo de dados a dados de multimídia, use a macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="19190-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="19190-118">Para obter mais informações sobre interfaces de fluxo de dados e arquivo, consulte [funções e macros do avifile](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="19190-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="19190-119">Antes de associar um novo arquivo ou dispositivo a uma janela MCIWnd, o [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) e o [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) fecham qualquer dispositivo atualmente associado à janela.</span><span class="sxs-lookup"><span data-stu-id="19190-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="19190-120">Seu aplicativo não precisa fechar nenhum dispositivo aberto antes de usar essas macros.</span><span class="sxs-lookup"><span data-stu-id="19190-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




