---
title: Automatizando a reprodução
description: Automatizando a reprodução
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Macro MCIWndCreate
- Macro MCIWndPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637093"
---
# <a name="automating-playback"></a><span data-ttu-id="fff9f-105">Automatizando a reprodução</span><span class="sxs-lookup"><span data-stu-id="fff9f-105">Automating Playback</span></span>

<span data-ttu-id="fff9f-106">Você pode automatizar a reprodução em seu aplicativo usando [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e a macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , juntamente com a macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="fff9f-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="fff9f-107">Para automatizar a reprodução, especifique os \_ estilos MCIWNDF NOPLAYBAR e MCIWNDF \_ notifymode no parâmetro \**MCIWndCreate \* \* \* dwStyle* .</span><span class="sxs-lookup"><span data-stu-id="fff9f-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="fff9f-108">Especifique o \_ estilo MCIWNDF NOPLAYBAR para ocultar a barra de ferramentas e o \_ estilo notifymode MCIWNDF para emitir uma mensagem de notificação apropriada quando o dispositivo parar de ser executado.</span><span class="sxs-lookup"><span data-stu-id="fff9f-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="fff9f-109">Você pode reproduzir o dispositivo ou o arquivo especificado em **MCIWndCreate** usando **MCIWndPlay**.</span><span class="sxs-lookup"><span data-stu-id="fff9f-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="fff9f-110">A macro MCIWndPlay começa a reproduzir o conteúdo de sua posição de reprodução atual e continua até seu fim.</span><span class="sxs-lookup"><span data-stu-id="fff9f-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="fff9f-111">Você pode destruir ou fechar uma janela do MCIWnd usando a macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="fff9f-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="fff9f-112">A macro **MCIWndDestroy** fecha o dispositivo ou arquivo e destrói a janela MCIWnd invalidando seu identificador.</span><span class="sxs-lookup"><span data-stu-id="fff9f-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="fff9f-113">Se seu aplicativo puder reutilizar a janela MCIWnd, use **MCIWndClose** para fechar o dispositivo sem destruir a janela.</span><span class="sxs-lookup"><span data-stu-id="fff9f-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="fff9f-114">Seu aplicativo pode detectar quando o dispositivo para de reproduzir e fechar automaticamente a janela.</span><span class="sxs-lookup"><span data-stu-id="fff9f-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="fff9f-115">Para fazer isso, especifique o \_ estilo notifymode MCIWNDF para o parâmetro *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="fff9f-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="fff9f-116">Isso faz com que o dispositivo envie uma mensagem [**MCIWNDM \_ notifymode**](mciwndm-notifymode.md) sempre que ele altera os modos.</span><span class="sxs-lookup"><span data-stu-id="fff9f-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="fff9f-117">Seu aplicativo pode interceptar esta mensagem para determinar se o dispositivo parou de ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="fff9f-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="fff9f-118">Quando o dispositivo para de ser executado, o aplicativo fecha a janela.</span><span class="sxs-lookup"><span data-stu-id="fff9f-118">When the device stops playing, the application closes the window.</span></span>

 

 




