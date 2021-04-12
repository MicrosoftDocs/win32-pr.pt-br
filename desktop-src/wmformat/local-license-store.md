---
title: Repositório de licenças local
description: Repositório de licenças local
ms.assetid: f50e4535-1d4d-4486-8308-c3314b1f5414
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d28703a0387d8676c4c8d5bf08f9e27a3ecf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364430"
---
# <a name="local-license-store"></a><span data-ttu-id="06e85-111">Repositório de licenças local</span><span class="sxs-lookup"><span data-stu-id="06e85-111">Local License Store</span></span>

<span data-ttu-id="06e85-112">Quando uma licença de DRM é entregue ao computador cliente, ela é colocada no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="06e85-112">When a DRM license is delivered to the client computer it is put into the local license store.</span></span> <span data-ttu-id="06e85-113">Esse é um arquivo protegido no disco rígido que contém todas as licenças emitidas para o usuário junto com outras informações de DRM.</span><span class="sxs-lookup"><span data-stu-id="06e85-113">This is a protected file on the hard disk that contains all the licenses issued to the user along with other DRM information.</span></span>

<span data-ttu-id="06e85-114">Você pode manipular dados no repositório de licenças local de algumas maneiras limitadas usando as APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06e85-114">You can manipulate data in the local license store in a few, limited ways by using the Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="06e85-115">Além do armazenamento de licença local, alguns objetos usam um armazenamento de licença temporário.</span><span class="sxs-lookup"><span data-stu-id="06e85-115">In addition to the local license store, some objects make use of a temporary license store.</span></span> <span data-ttu-id="06e85-116">Uma licença em um repositório temporário existe apenas por um curto período de tempo.</span><span class="sxs-lookup"><span data-stu-id="06e85-116">A license in a temporary store exists only for a short period of time.</span></span> <span data-ttu-id="06e85-117">No entanto, algumas licenças que começam em um repositório temporário podem ser salvas no armazenamento de licença local normal.</span><span class="sxs-lookup"><span data-stu-id="06e85-117">However, some licenses that begin in a temporary store can be saved to the regular local license store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06e85-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06e85-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e85-119">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="06e85-119">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




