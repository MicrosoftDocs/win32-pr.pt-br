---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292244"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="0a426-103">VariantNotInt (CheckRole)</span><span class="sxs-lookup"><span data-stu-id="0a426-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="0a426-104">Texto</span><span class="sxs-lookup"><span data-stu-id="0a426-104">Text</span></span>

<span data-ttu-id="0a426-105">A variante retornada de {0} deve ser um {1} , mas é um {2} .</span><span class="sxs-lookup"><span data-stu-id="0a426-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="0a426-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a426-106">Type</span></span>

<span data-ttu-id="0a426-107">Erro</span><span class="sxs-lookup"><span data-stu-id="0a426-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0a426-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a426-108">Description</span></span>

<span data-ttu-id="0a426-109">Um elemento está relatando uma função de MSAA inválida.</span><span class="sxs-lookup"><span data-stu-id="0a426-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="0a426-110">Por exemplo, o método [**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) usado para recuperar a função MSAA de um elemento deve retornar um valor inteiro que representa uma das constantes da função MSAA, mas que está retornando outra variante em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0a426-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="0a426-111">Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque os elementos podem ser identificados incorretamente para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0a426-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0a426-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="0a426-112">Possible causes</span></span>

<span data-ttu-id="0a426-113">O elemento ou seu pai tem uma função de MSAA definida incorretamente.</span><span class="sxs-lookup"><span data-stu-id="0a426-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a426-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a426-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a426-115">**IAccessible:: obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="0a426-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="0a426-116">**Funções de objeto**</span><span class="sxs-lookup"><span data-stu-id="0a426-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




