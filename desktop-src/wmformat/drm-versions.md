---
title: Versões de DRM
description: Versões de DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- SDK do Windows Media Format, versões do DRM
- DRM (gerenciamento de direitos digitais), versões
- DRM (gerenciamento de direitos digitais), versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916129"
---
# <a name="drm-versions"></a><span data-ttu-id="496bd-106">Versões de DRM</span><span class="sxs-lookup"><span data-stu-id="496bd-106">DRM Versions</span></span>

<span data-ttu-id="496bd-107">Há várias versões do DRM (gerenciamento de direitos digitais) do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="496bd-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="496bd-108">A versão 1 do DRM é muitas vezes separada das outras versões nesta documentação, pois ela é implementada usando técnicas que são diferentes das versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="496bd-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="496bd-109">A segunda geração do Windows Media DRM é chamada de DRM versão 7 porque foi introduzida como parte do SDK do Windows Media Format 7.</span><span class="sxs-lookup"><span data-stu-id="496bd-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="496bd-110">Às vezes, ele é chamado de DRM versão 2.</span><span class="sxs-lookup"><span data-stu-id="496bd-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="496bd-111">As versões posteriores do Windows Media DRM, DRM versão 9 e o novo Windows Media DRM 10, são extensões do DRM versão 7 e usam os mesmos procedimentos para implementação.</span><span class="sxs-lookup"><span data-stu-id="496bd-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="496bd-112">Todas as versões do Windows Media DRM usam as mesmas rotinas de criptografia; as diferenças entre as versões têm a ver com os recursos de licença.</span><span class="sxs-lookup"><span data-stu-id="496bd-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="496bd-113">Ao criar arquivos protegidos usando os objetos do Windows Media Format SDK, você deve dar suporte tanto à versão 1 quanto à versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="496bd-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="496bd-114">Os arquivos protegidos pela versão 1 do DRM diferem dos arquivos protegidos por versões posteriores apenas no conteúdo do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="496bd-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="496bd-115">Os arquivos mais recentes que contêm as informações adicionais de cabeçalho ainda podem ser usados em clientes que processam apenas conteúdo da versão 1.</span><span class="sxs-lookup"><span data-stu-id="496bd-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="496bd-116">Embora as versões posteriores do DRM ofereçam um nível mais alto de segurança e recursos adicionais, ainda há muitos players que usam apenas a versão 1.</span><span class="sxs-lookup"><span data-stu-id="496bd-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="496bd-117">Para obter mais informações sobre versões de DRM, consulte a documentação do SDK do Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="496bd-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="496bd-118">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="496bd-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="496bd-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="496bd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="496bd-120">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="496bd-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="496bd-121">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="496bd-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




