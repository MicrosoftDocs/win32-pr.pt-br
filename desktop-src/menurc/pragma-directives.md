---
title: Diretivas pragma
description: O RC não oferece suporte às diretivas pragma com suporte pelo compilador C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007525"
---
# <a name="pragma-directives"></a><span data-ttu-id="691f1-103">Diretivas pragma</span><span class="sxs-lookup"><span data-stu-id="691f1-103">Pragma Directives</span></span>

<span data-ttu-id="691f1-104">O RC não oferece suporte às diretivas pragma com suporte pelo compilador C/C++.</span><span class="sxs-lookup"><span data-stu-id="691f1-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="691f1-105">No entanto, o RC oferece suporte à seguinte diretiva pragma para alterar a página de código:</span><span class="sxs-lookup"><span data-stu-id="691f1-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="691f1-106">Não há suporte para esse pragma em um arquivo de recurso incluído (. rc).</span><span class="sxs-lookup"><span data-stu-id="691f1-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="691f1-107">Portanto, se você tiver um arquivo pai. rc e ele incluir arquivos. rc para vários idiomas, use esse pragma antes de incluir outro arquivo. RC em vez de usá-lo no próprio arquivo. rc incluído.</span><span class="sxs-lookup"><span data-stu-id="691f1-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="691f1-108">Isso é demonstrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="691f1-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="691f1-109">Para obter uma lista de valores para CodePageNum, consulte [identificadores de página de código](../intl/code-page-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="691f1-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 