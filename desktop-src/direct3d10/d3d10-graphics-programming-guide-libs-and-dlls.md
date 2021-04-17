---
description: Para que um aplicativo seja executado corretamente, o computador host deve ter as DLLs apropriadas instaladas. Essas DLLs podem ser fornecidas pelo sistema operacional ou pelo pacote redistribuível dos aplicativos.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Vinculando bibliotecas estáticas e dinâmicas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813310"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="43586-104">Vinculando bibliotecas estáticas e dinâmicas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43586-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="43586-105">Para que um aplicativo seja executado corretamente, o computador host deve ter as DLLs apropriadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="43586-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="43586-106">Essas DLLs podem ser fornecidas pelo sistema operacional ou pelo pacote redistribuível dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="43586-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="43586-107">Bibliotecas carregam DLLs apropriadas</span><span class="sxs-lookup"><span data-stu-id="43586-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="43586-108">As bibliotecas incluídas no SDK do DirectX carregarão automaticamente as DLLs apropriadas no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="43586-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="43586-109">A exceção a essa regra é d3dx10. lib/d3dx10d. lib, que carregará o d3dx10.dll enviado com essa versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="43586-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="43586-110">Por exemplo, se o SDK baixado incluir d3dx10 \_33.dll e d3dx10 \_34.dll, a biblioteca (d3dx10. lib) que foi enviada com esse SDK carregará d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="43586-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="43586-111">Se um SDK subsequente for instalado mais tarde contendo d3dx10 \_ 35. lib, o d3dx10. lib do SDK anterior ainda carregará d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="43586-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="43586-112">O d3dx10. lib do SDK mais recente irá carregar o d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="43586-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="43586-113">Redistribuindo binários</span><span class="sxs-lookup"><span data-stu-id="43586-113">Redistributing Binaries</span></span>

<span data-ttu-id="43586-114">Somente d3dx10.dll (e as versões subsequentes do mesmo arquivo) podem ser redistribuídas.</span><span class="sxs-lookup"><span data-stu-id="43586-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="43586-115">Para redistribuir esse arquivo, você deve usar a função **DirectXSetup** .</span><span class="sxs-lookup"><span data-stu-id="43586-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="43586-116">Para obter detalhes sobre como usar essa função e como reunir um pacote redistribuível, consulte [instalando o DirectX com DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="43586-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="43586-117">Todos os outros binários necessários estão incluídos no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="43586-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="43586-118">Os únicos binários que podem ser redistribuídos são os localizados no diretório a seguir.</span><span class="sxs-lookup"><span data-stu-id="43586-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="43586-119">A tabela a seguir descreve os binários dos quais os desenvolvedores devem estar cientes.</span><span class="sxs-lookup"><span data-stu-id="43586-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="43586-120">Binários do Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="43586-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="43586-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="43586-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43586-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="43586-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="43586-123">Componentes de D3DX10 de varejo e depuração; os componentes de varejo podem ser redistribuídos no CAB Redist.</span><span class="sxs-lookup"><span data-stu-id="43586-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="43586-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="43586-124">d3d10ref.dll</span></span>           | <span data-ttu-id="43586-125">Rasterizador de referência.</span><span class="sxs-lookup"><span data-stu-id="43586-125">Reference Rasterizer.</span></span> <span data-ttu-id="43586-126">Fornece a implementação de software do pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="43586-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="43586-127">Incluído apenas como parte do SDK do Windows ou SDK herdado do DirectX e não pode ser redistribuído.</span><span class="sxs-lookup"><span data-stu-id="43586-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="43586-128">O rasterizador de referência destina-se somente à depuração.</span><span class="sxs-lookup"><span data-stu-id="43586-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="43586-129">A vinculação explícita não é necessária; a tentativa de criar um dispositivo de referência (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) carregará essa dll, se ela estiver presente.</span><span class="sxs-lookup"><span data-stu-id="43586-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="43586-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="43586-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="43586-131">Uma série de utilitários do SDK que atuam como uma camada entre chamadas de API e execução em tempo de execução, incluindo a [camada de depuração](d3d10-graphics-programming-guide-api-features-layers.md) e a camada de switch-to-Reference.</span><span class="sxs-lookup"><span data-stu-id="43586-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="43586-132">A vinculação explícita não é necessária; se um dispositivo for criado com o sinalizador de camada apropriado, essa DLL será carregada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="43586-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="43586-133">Esse componente destina-se apenas a fins de desenvolvimento e depuração.</span><span class="sxs-lookup"><span data-stu-id="43586-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="43586-134">Incluído apenas como parte do SDK do Windows ou SDK herdado do DirectX e não pode ser redistribuído.</span><span class="sxs-lookup"><span data-stu-id="43586-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43586-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43586-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43586-136">Guia de programação para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="43586-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="43586-137">Gráficos do Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="43586-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



