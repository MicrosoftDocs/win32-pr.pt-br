---
title: Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D
description: Esta seção aborda técnicas de interoperabilidade com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portabilidade do Direct3D 11 para o Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103433"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="e11d0-103">Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D</span><span class="sxs-lookup"><span data-stu-id="e11d0-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="e11d0-104">Esta seção aborda técnicas de interoperabilidade com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portabilidade do Direct3D 11 para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e11d0-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e11d0-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e11d0-105">In this section</span></span>



| <span data-ttu-id="e11d0-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="e11d0-106">Topic</span></span>                                                                                             | <span data-ttu-id="e11d0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e11d0-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e11d0-108">Interoperabilidade do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e11d0-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="e11d0-109">D3D12 pode ser usado para gravar aplicativos divididos em componentes.</span><span class="sxs-lookup"><span data-stu-id="e11d0-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="e11d0-110">Direct3D 11 on 12</span><span class="sxs-lookup"><span data-stu-id="e11d0-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="e11d0-111">D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos do D3D11 para direcionar a API D3D12.</span><span class="sxs-lookup"><span data-stu-id="e11d0-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="e11d0-112">O D3D11on12 permite que os componentes escritos usando D3D11 (por exemplo, texto e interface do usuário D2D) trabalhem em conjunto com os componentes criados direcionando a API do D3D12.</span><span class="sxs-lookup"><span data-stu-id="e11d0-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="e11d0-113">O D3D11on12 também permite portabilidade incremental de um aplicativo do D3D11 para o D3D12, permitindo que partes do aplicativo continuem direcionando para a D3D11 para simplificar enquanto outras voltam a D3D12 para desempenho, enquanto sempre têm renderização completa e correta.</span><span class="sxs-lookup"><span data-stu-id="e11d0-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="e11d0-114">O D3D11On12 torna mais simples do que usar técnicas de interoperabilidade para compartilhar recursos e sincronizar o trabalho entre as duas APIs.</span><span class="sxs-lookup"><span data-stu-id="e11d0-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="e11d0-115">Portar do Direct3D 11 para o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e11d0-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="e11d0-116">Esta seção fornece algumas diretrizes sobre como portar de um mecanismo de gráficos do Direct3D 11 personalizado para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e11d0-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="e11d0-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e11d0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11d0-118">Guia de programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e11d0-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





