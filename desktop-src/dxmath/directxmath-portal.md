---
description: DirectXMath
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd35f1faf004bc55a6802da204a6c2fe4e7869b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113004"
---
# <a name="directxmath"></a><span data-ttu-id="f9c43-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f9c43-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="f9c43-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="f9c43-104">Purpose</span></span>

<span data-ttu-id="f9c43-105">A API do DirectXMath fornece tipos e funções de C++ para dispositivos baseados em SIMD para operações matemáticas de Algebra e gráficos comuns comuns a aplicativos do DirectX.</span><span class="sxs-lookup"><span data-stu-id="f9c43-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="f9c43-106">A biblioteca fornece versões otimizadas para Windows 32 bits (x86), Windows 64 bits (x64) e Windows no ARM/ARM64 por meio do suporte a SSE, AVX e ARM-NEON intrínsecos no compilador Visual C++.</span><span class="sxs-lookup"><span data-stu-id="f9c43-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="f9c43-107">Para os desenvolvedores novos no DirectXMath, talvez você queira considerar o uso do invólucro SimpleMath no *Kit de ferramentas DirectX* para [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="f9c43-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f9c43-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f9c43-108">In this section</span></span>



| <span data-ttu-id="f9c43-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="f9c43-109">Topic</span></span>                                                                     | <span data-ttu-id="f9c43-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c43-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="f9c43-111">Guia de programação do DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f9c43-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="f9c43-112">O DirectXMath fornece uma solução matemática otimizada para o Windows.</span><span class="sxs-lookup"><span data-stu-id="f9c43-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="f9c43-113">Referência de programação DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f9c43-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="f9c43-114">Esta seção contém material de referência para a biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="f9c43-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="f9c43-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="f9c43-115">Developer audience</span></span>

<span data-ttu-id="f9c43-116">A biblioteca DirectXMath foi projetada para desenvolvedores de C++ que trabalham em jogos e elementos gráficos do DirectX em aplicativos da Windows Store, jogos do Xbox e aplicativos de área de trabalho tradicionais para Windows.</span><span class="sxs-lookup"><span data-stu-id="f9c43-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="f9c43-117">Obtendo DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f9c43-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="f9c43-118">Os cabeçalhos DirectXMath são fornecidos no SDK do Windows fornecido com o Visual Studio 2012 ou posterior, e como um cabeçalho embutido, não há nenhuma DLL ou biblioteca estática a ser vinculada.</span><span class="sxs-lookup"><span data-stu-id="f9c43-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="f9c43-119">Ele também está disponível como um pacote no [NuGet](https://www.nuget.org/packages/directxmath/).</span><span class="sxs-lookup"><span data-stu-id="f9c43-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="f9c43-120">DirectXMath é código-fonte aberto sob a [licença MIT](https://opensource.org/licenses/MIT) hospedada no [GitHub](https://github.com/Microsoft/DirectXMath).</span><span class="sxs-lookup"><span data-stu-id="f9c43-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




