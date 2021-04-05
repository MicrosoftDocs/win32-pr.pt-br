---
description: Uma DLL (biblioteca de vínculo dinâmico) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliotecas de Dynamic-Link (bibliotecas de vínculo dinâmico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647720"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="23c42-103">Bibliotecas de Dynamic-Link (bibliotecas de vínculo dinâmico)</span><span class="sxs-lookup"><span data-stu-id="23c42-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="23c42-104">Uma dll ( *biblioteca de vínculo dinâmico* ) é um módulo que contém funções e dados que podem ser usados por outro módulo (aplicativo ou dll).</span><span class="sxs-lookup"><span data-stu-id="23c42-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="23c42-105">Uma DLL pode definir dois tipos de funções: exportadas e internas.</span><span class="sxs-lookup"><span data-stu-id="23c42-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="23c42-106">As funções exportadas são destinadas a serem chamadas por outros módulos, bem como de dentro da DLL em que são definidas.</span><span class="sxs-lookup"><span data-stu-id="23c42-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="23c42-107">Normalmente, as funções internas devem ser chamadas somente de dentro da DLL em que são definidas.</span><span class="sxs-lookup"><span data-stu-id="23c42-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="23c42-108">Embora uma DLL possa exportar dados, os dados geralmente são usados apenas por suas funções.</span><span class="sxs-lookup"><span data-stu-id="23c42-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="23c42-109">No entanto, não há nada para impedir que outro módulo leia ou grave esse endereço.</span><span class="sxs-lookup"><span data-stu-id="23c42-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="23c42-110">As DLLs fornecem uma maneira de modularizar aplicativos para que sua funcionalidade possa ser atualizada e reutilizada com mais facilidade.</span><span class="sxs-lookup"><span data-stu-id="23c42-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="23c42-111">As DLLs também ajudam a reduzir a sobrecarga de memória quando vários aplicativos usam a mesma funcionalidade ao mesmo tempo, porque, embora cada aplicativo receba sua própria cópia dos dados de DLL, os aplicativos compartilham o código de DLL.</span><span class="sxs-lookup"><span data-stu-id="23c42-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="23c42-112">A API (interface de programação de aplicativo) do Windows é implementada como um conjunto de DLLs, de modo que qualquer processo que usa a API do Windows usa vinculação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="23c42-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="23c42-113">Sobre bibliotecas de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="23c42-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="23c42-114">Usando bibliotecas de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="23c42-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="23c42-115">Referência da biblioteca de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="23c42-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="23c42-116">Se você for um usuário tendo dificuldades com uma DLL em seu computador, deverá entrar em contato com o atendimento ao cliente para o fornecedor de software que publica a DLL.</span><span class="sxs-lookup"><span data-stu-id="23c42-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="23c42-117">Se você sentir que precisa de suporte para um produto da Microsoft (incluindo o Windows), acesse nosso site de suporte técnico em [support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="23c42-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="23c42-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23c42-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c42-119">DLLs (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="23c42-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
