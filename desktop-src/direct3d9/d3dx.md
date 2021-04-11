---
description: D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidade gráfica adicional sobre o Direct3D. D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296091"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="06bca-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06bca-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="06bca-105">D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidade gráfica adicional sobre o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="06bca-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="06bca-106">D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="06bca-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="06bca-107">Apenas uma versão do D3DX é fornecida nesta versão do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="06bca-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="06bca-108">A DLL de D3DX de varejo está incluída no redistribuível fornecido no SDK e é instalada automaticamente como parte da [instalação do DirectX com DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="06bca-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="06bca-109">A biblioteca D3DX incluída nesta versão depende dos tempos de execução do Direct3D fornecidos com esse SDK.</span><span class="sxs-lookup"><span data-stu-id="06bca-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="06bca-110">Os aplicativos que se vinculam à versão do D3DX nesta versão também devem redistribuir o tempo de execução desse SDK.</span><span class="sxs-lookup"><span data-stu-id="06bca-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="06bca-111">Várias versões do D3DX podem residir de forma independente em um único sistema simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="06bca-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="06bca-112">Ao vincular estaticamente um aplicativo a D3dx9. lib, o aplicativo é vinculado dinamicamente à DLL de varejo D3DX correspondente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="06bca-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="06bca-113">Essa DLL corresponde aos cabeçalhos D3DX em que o aplicativo é compilado (nomeado com a constante de versão do SDK do D3DX \_ \_ em D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="06bca-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="06bca-114">À medida que novas versões do D3DX forem enviadas em versões futuras do SDK do DirectX, os aplicativos que se vinculam a bibliotecas anteriores do D3DX permanecerão inalterados.</span><span class="sxs-lookup"><span data-stu-id="06bca-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="06bca-115">A biblioteca D3DX aborda essas áreas gerais de funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="06bca-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="06bca-116">Suporte de desenho de linha no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06bca-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="06bca-117">Suporte a malha no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06bca-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="06bca-118">Suporte à função matemática no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06bca-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="06bca-119">Suporte a textura em D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06bca-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="06bca-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06bca-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bca-121">Introdução</span><span class="sxs-lookup"><span data-stu-id="06bca-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



