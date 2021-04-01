---
title: Ações e direitos
description: Ações e direitos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004986"
---
# <a name="actions-and-rights"></a><span data-ttu-id="5942c-113">Ações e direitos</span><span class="sxs-lookup"><span data-stu-id="5942c-113">Actions and Rights</span></span>

<span data-ttu-id="5942c-114">Quando um arquivo é protegido usando o Windows Media DRM, seu uso é completamente restrito.</span><span class="sxs-lookup"><span data-stu-id="5942c-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="5942c-115">As licenças podem ser emitidas para permitir que um usuário use o conteúdo de maneiras específicas.</span><span class="sxs-lookup"><span data-stu-id="5942c-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="5942c-116">Cada modo no qual um usuário pode usar o conteúdo é descrito por uma ação.</span><span class="sxs-lookup"><span data-stu-id="5942c-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="5942c-117">Por exemplo, reproduzir um arquivo em um computador é uma ação.</span><span class="sxs-lookup"><span data-stu-id="5942c-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="5942c-118">Uma licença que habilita uma determinada ação é considerada para conceder um direito.</span><span class="sxs-lookup"><span data-stu-id="5942c-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="5942c-119">Por exemplo, uma licença pode conceder o direito de reproduzir conteúdo em um computador.</span><span class="sxs-lookup"><span data-stu-id="5942c-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="5942c-120">Ações e direitos referem-se às mesmas maneiras de usar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5942c-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="5942c-121">A diferença é que a ação refere-se ao uso enquanto a direita se refere à permissão.</span><span class="sxs-lookup"><span data-stu-id="5942c-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="5942c-122">Apesar dessa distinção, a ação de palavras e a direita costumam ser usadas de forma intercambiável nesta documentação e em outros documentos que descrevem o DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5942c-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="5942c-123">As ações governadas pelos direitos de DRM do Windows Media são listadas na seção [constantes de direitos](rights-constants.md) desta documentação.</span><span class="sxs-lookup"><span data-stu-id="5942c-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="5942c-124">Determinados métodos das APIs estendidas do cliente DRM do Windows Media usam constantes diferentes para se referir aos direitos de DRM básicos.</span><span class="sxs-lookup"><span data-stu-id="5942c-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="5942c-125">Por exemplo, o método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa um conjunto de cadeias de caracteres específicas para Estados de licença.</span><span class="sxs-lookup"><span data-stu-id="5942c-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="5942c-126">Mesmo que essas constantes estejam definindo cadeias de caracteres diferentes das constantes de direitos básicas, elas se referem aos mesmos direitos na licença.</span><span class="sxs-lookup"><span data-stu-id="5942c-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5942c-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5942c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5942c-128">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="5942c-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




