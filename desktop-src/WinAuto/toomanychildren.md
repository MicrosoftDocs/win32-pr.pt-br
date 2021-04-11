---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159887"
---
# <a name="toomanychildren"></a><span data-ttu-id="5a1e6-103">TooManyChildren</span><span class="sxs-lookup"><span data-stu-id="5a1e6-103">TooManyChildren</span></span>

## <a name="text"></a><span data-ttu-id="5a1e6-104">Texto</span><span class="sxs-lookup"><span data-stu-id="5a1e6-104">Text</span></span>

<span data-ttu-id="5a1e6-105">Parou de procurar irmãos adicionais depois de encontrar {0} irmãos.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-105">Stopped looking for additional siblings after finding {0} siblings.</span></span> <span data-ttu-id="5a1e6-106">Possível árvore incorreta</span><span class="sxs-lookup"><span data-stu-id="5a1e6-106">Possible incorrect tree</span></span>

## <a name="type"></a><span data-ttu-id="5a1e6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a1e6-107">Type</span></span>

<span data-ttu-id="5a1e6-108">Aviso</span><span class="sxs-lookup"><span data-stu-id="5a1e6-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="5a1e6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a1e6-109">Description</span></span>

<span data-ttu-id="5a1e6-110">A árvore de elementos pode ser cíclica e a profundidade da árvore é infinita.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-110">The element tree might be cyclic and the tree depth infinite.</span></span>

<span data-ttu-id="5a1e6-111">Esse problema pode causar problemas de navegação para ferramentas automatizadas porque elas irão inserir o que parece ser uma referência circular ou um loop infinito.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-111">This issue can cause navigation problems for automated tools because they will enter what appears to be a circular reference or infinite loop.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="5a1e6-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="5a1e6-112">Possible causes</span></span>

-   <span data-ttu-id="5a1e6-113">O design de aplicativo ou de controle pode ser muito complexo.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-113">Application or control design may be too complex.</span></span> <span data-ttu-id="5a1e6-114">Esse aviso pode ser relatado para controles de exibição de lista que têm um grande número de itens.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-114">This warning might be reported for list-view controls that have a large number of items.</span></span> <span data-ttu-id="5a1e6-115">Nesses casos, normalmente você pode ignorar esse aviso.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-115">In these cases, you can typically ignore this warning.</span></span>
-   <span data-ttu-id="5a1e6-116">Uma implementação de MSAA incorreta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-116">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a1e6-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a1e6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a1e6-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="5a1e6-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




