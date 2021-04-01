---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159824"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="32b30-103">VariantNotInt (CheckState)</span><span class="sxs-lookup"><span data-stu-id="32b30-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="32b30-104">Texto</span><span class="sxs-lookup"><span data-stu-id="32b30-104">Text</span></span>

<span data-ttu-id="32b30-105">A variante retornada de {0} deve ser um {1} , mas é um {2} .</span><span class="sxs-lookup"><span data-stu-id="32b30-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="32b30-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="32b30-106">Type</span></span>

<span data-ttu-id="32b30-107">Erro</span><span class="sxs-lookup"><span data-stu-id="32b30-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="32b30-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="32b30-108">Description</span></span>

<span data-ttu-id="32b30-109">Um elemento está relatando um estado de MSAA inválido.</span><span class="sxs-lookup"><span data-stu-id="32b30-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="32b30-110">Por exemplo, o método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usado para recuperar o estado de MSAA de um elemento deve retornar um valor inteiro que representa uma das constantes de estado de MSAA, mas está retornando outra variante em vez disso.</span><span class="sxs-lookup"><span data-stu-id="32b30-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="32b30-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um estado de elemento incorreto pode ser relatado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="32b30-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="32b30-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="32b30-112">Possible causes</span></span>

<span data-ttu-id="32b30-113">O elemento ou seu pai tem um estado de MSAA definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="32b30-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32b30-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32b30-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b30-115">**IAccessible:: obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="32b30-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="32b30-116">**Constantes de estado do objeto**</span><span class="sxs-lookup"><span data-stu-id="32b30-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




