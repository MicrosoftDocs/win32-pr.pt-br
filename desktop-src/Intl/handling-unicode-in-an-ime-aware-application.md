---
description: Lidando com Unicode em um aplicativo IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Lidando com Unicode em um aplicativo IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761832"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="5ca27-103">Lidando com Unicode em um aplicativo IME-Aware</span><span class="sxs-lookup"><span data-stu-id="5ca27-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="5ca27-104">Dois problemas estão envolvidos no IMM e seu manuseio de Unicode.</span><span class="sxs-lookup"><span data-stu-id="5ca27-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="5ca27-105">O primeiro problema é que as versões Unicode das funções do IMM recuperam o tamanho de um buffer em bytes em vez de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5ca27-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="5ca27-106">O segundo problema é que o IMM normalmente recupera caracteres Unicode (em vez de caracteres DBCS) nas mensagens de caracteres do [**WM \_ Char**](../inputdev/wm-char.md) e do [**\_ \_ IME do WM**](wm-ime-char.md) .</span><span class="sxs-lookup"><span data-stu-id="5ca27-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="5ca27-107">O Windows dá suporte a uma interface Unicode para o IMM, além da interface ANSI com suporte originalmente.</span><span class="sxs-lookup"><span data-stu-id="5ca27-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="5ca27-108">Seus aplicativos devem usar [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) para fazer com que as mensagens de caracteres do [**WM \_ Char**](../inputdev/wm-char.md) e do [**\_ IME \_ do WM**](wm-ime-char.md) recuperem caracteres Unicode em vez de caracteres DBCS no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5ca27-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ca27-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ca27-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ca27-110">Usando o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5ca27-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
