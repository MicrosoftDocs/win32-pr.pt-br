---
description: Quando o aplicativo está lidando com palavras inteiras, as posições válidas para o cursor são marcadas pelo valor do membro fWordStop da \_ estrutura LOGATTR do script. Esse valor é recuperado fazendo uma chamada para ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Usando pontos de quebra de palavras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172172"
---
# <a name="using-word-break-points"></a><span data-ttu-id="82a44-104">Usando pontos de quebra de palavras</span><span class="sxs-lookup"><span data-stu-id="82a44-104">Using Word Break Points</span></span>

<span data-ttu-id="82a44-105">Quando o aplicativo está lidando com palavras inteiras, as posições válidas para o cursor são marcadas pelo valor do membro **fWordStop** da estrutura [**\_ LOGATTR do script**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="82a44-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="82a44-106">Esse valor é recuperado fazendo uma chamada para [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="82a44-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="82a44-107">Posições válidas para linhas de quebra entre palavras são marcadas pelo valor **fSoftBreak** recuperado por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="82a44-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82a44-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82a44-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a44-109">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="82a44-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



