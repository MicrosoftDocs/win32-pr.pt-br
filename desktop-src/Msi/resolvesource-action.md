---
description: A ação resolver determina o local da origem e define a propriedade SourceDir se a fonte ainda não tiver sido resolvida.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Ação resolver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787494"
---
# <a name="resolvesource-action"></a><span data-ttu-id="872b1-103">Ação resolver</span><span class="sxs-lookup"><span data-stu-id="872b1-103">ResolveSource Action</span></span>

<span data-ttu-id="872b1-104">A ação resolver determina o local da origem e define a propriedade [**SourceDir**](sourcedir.md) se a fonte ainda não tiver sido resolvida.</span><span class="sxs-lookup"><span data-stu-id="872b1-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="872b1-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="872b1-105">Sequence Restrictions</span></span>

<span data-ttu-id="872b1-106">A ação de resolução deve vir após a [ação CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="872b1-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="872b1-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="872b1-107">ActionData Messages</span></span>

<span data-ttu-id="872b1-108">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="872b1-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="872b1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="872b1-109">Remarks</span></span>

<span data-ttu-id="872b1-110">A ação de resolução deve ser chamada antes de usar a propriedade [**SourceDir**](sourcedir.md) em qualquer expressão.</span><span class="sxs-lookup"><span data-stu-id="872b1-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="872b1-111">Ele também deve ser chamado antes de tentar recuperar o valor da propriedade **SourceDir** usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="872b1-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="872b1-112">A ação de resolução não deve ser executada quando a origem não estiver disponível, pois pode ser ao desinstalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="872b1-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="872b1-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="872b1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872b1-114">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="872b1-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



