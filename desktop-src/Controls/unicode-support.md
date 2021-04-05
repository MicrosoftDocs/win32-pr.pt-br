---
title: Suporte a Unicode para controles comuns
description: Este tópico descreve como dar suporte a Unicode para notificações de controle comuns.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917801"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="94d00-103">Suporte a Unicode para controles comuns</span><span class="sxs-lookup"><span data-stu-id="94d00-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="94d00-104">Este tópico descreve como dar suporte a Unicode para notificações de controle comuns.</span><span class="sxs-lookup"><span data-stu-id="94d00-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="94d00-105">Para as versões 5,80 e posteriores do comctl32.dll, as notificações de controles comuns dão suporte a formatos ANSI e Unicode em sistemas Windows 95 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="94d00-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="94d00-106">O sistema determina qual formato usar enviando a janela uma mensagem do [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) .</span><span class="sxs-lookup"><span data-stu-id="94d00-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="94d00-107">Para especificar um formato, retorne o NFR \_ ANSI para notificações ANSI ou o NFR \_ Unicode para notificações Unicode.</span><span class="sxs-lookup"><span data-stu-id="94d00-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="94d00-108">Se você não tratar essa mensagem, o sistema chamará [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar o formato.</span><span class="sxs-lookup"><span data-stu-id="94d00-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="94d00-109">Como o Windows 95 e o Windows 98 sempre retornam **false** para essa chamada de função, eles usam notificações ANSI por padrão.</span><span class="sxs-lookup"><span data-stu-id="94d00-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94d00-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94d00-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94d00-111">Sobre controles comuns</span><span class="sxs-lookup"><span data-stu-id="94d00-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 