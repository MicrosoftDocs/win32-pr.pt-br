---
description: O D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidades gráficas adicionais sobre o Direct3D. O D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910250"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="43970-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43970-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="43970-105">A biblioteca D3DX foi preterida.</span><span class="sxs-lookup"><span data-stu-id="43970-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="43970-106">Se atualizar para uma versão mais recente do Direct3D e o código do utilitário associado não for uma opção, você poderá usar o pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) em vez de depender do SDK do DirectX herdado ou do DirectSetup.</span><span class="sxs-lookup"><span data-stu-id="43970-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="43970-107">O D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidades gráficas adicionais sobre o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="43970-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="43970-108">O D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="43970-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="43970-109">Apenas uma versão do D3DX é fornecida nesta versão do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="43970-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="43970-110">A DLL D3DX de varejo está incluída no redistribuível fornecido no SDK e é instalada automaticamente como parte da instalação do **DirectX com DirectSetup.**</span><span class="sxs-lookup"><span data-stu-id="43970-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="43970-111">A biblioteca D3DX incluída nesta versão depende dos runtimes do Direct3D fornecidos com esse SDK.</span><span class="sxs-lookup"><span data-stu-id="43970-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="43970-112">Os aplicativos que se vinculam à versão do D3DX nesta versão também devem redistribuir o runtime desse SDK.</span><span class="sxs-lookup"><span data-stu-id="43970-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="43970-113">Várias versões do D3DX podem residir de forma independente em um único sistema simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="43970-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="43970-114">Vinculando estaticamente um aplicativo a D3dx9.lib, o aplicativo vincula dinamicamente à DLL DLL D3DX de varejo correspondente em tempo de run-time.</span><span class="sxs-lookup"><span data-stu-id="43970-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="43970-115">Essa DLL corresponde aos headers D3DX em que o aplicativo é compilado (nomeado com a constante VERSION do SDK do D3DX \_ \_ em D3dx9core.h).</span><span class="sxs-lookup"><span data-stu-id="43970-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="43970-116">À medida que novas versões do D3DX são enviadas em versões futuras do SDK do DirectX, os aplicativos que se vinculam a bibliotecas D3DX anteriores permanecerão inalterados.</span><span class="sxs-lookup"><span data-stu-id="43970-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="43970-117">A biblioteca D3DX aborda essas áreas gerais de funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="43970-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="43970-118">Suporte a desenho de linha no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43970-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="43970-119">Suporte à malha no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43970-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="43970-120">Suporte à função matemática no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43970-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="43970-121">Suporte à textura no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43970-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="43970-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43970-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43970-123">Introdução</span><span class="sxs-lookup"><span data-stu-id="43970-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



