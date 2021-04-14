---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivos MCI, Driver MCIAVI
- Comandos MCI, Driver MCIAVI
- Driver MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453653"
---
# <a name="mciavi"></a><span data-ttu-id="93e94-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="93e94-106">MCIAVI</span></span>

<span data-ttu-id="93e94-107">Um arquivo AVI pode conter mais de dois fluxos — por exemplo, uma sequência de vídeo, uma trilha sonora em inglês e uma trilha sonora francesa.</span><span class="sxs-lookup"><span data-stu-id="93e94-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="93e94-108">Seu aplicativo pode usar um fluxo independentemente dos outros fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="93e94-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="93e94-109">O tipo de dispositivo **DigitalVideo** controla arquivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93e94-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="93e94-110">Para obter uma lista dos comandos MCI reconhecidos por dispositivos de vídeo digital, consulte [conjunto de comandos de vídeo digital](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="93e94-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="93e94-111">O driver MCIAVI reproduz sequências de vídeo e outros fluxos de dados sob o controle de comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="93e94-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="93e94-112">Os fluxos de dados podem conter imagens, áudio e paletas.</span><span class="sxs-lookup"><span data-stu-id="93e94-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="93e94-113">Os dados da imagem podem consistir em imagens com paletas de cores ou informações true-color.</span><span class="sxs-lookup"><span data-stu-id="93e94-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="93e94-114">O áudio é sincronizado com o vídeo dentro de um thirtieth de um segundo.</span><span class="sxs-lookup"><span data-stu-id="93e94-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="93e94-115">No entanto, se o hardware de áudio não estiver disponível, o driver reproduzirá apenas o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93e94-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="93e94-116">O driver MCIAVI pode descartar quadros de vídeo, se necessário, para reproduzir um fluxo sem interrupção de áudio.</span><span class="sxs-lookup"><span data-stu-id="93e94-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="93e94-117">Seu aplicativo pode usar os serviços de classe de janela MCIWnd em vez da interface de comando MCI para controlar qualquer driver MCI.</span><span class="sxs-lookup"><span data-stu-id="93e94-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="93e94-118">Essa classe de janela lida com muitos dos detalhes do gerenciamento da janela que oferece suporte ao dispositivo MCI e simplifica a programação necessária para enviar os comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="93e94-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="93e94-119">Seu aplicativo pode usar os serviços de biblioteca do MCIWnd diretamente para controlar o dispositivo MCI ou pode ter MCIWnd exibir uma barra de ferramentas, barra de rolagem e menus que permitem ao usuário controlar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93e94-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="93e94-120">Para obter mais informações sobre a classe de janela MCIWnd, consulte [classe de janela MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="93e94-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




