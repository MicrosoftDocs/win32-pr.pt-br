---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637133"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="9541f-103">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="9541f-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="9541f-104">Texto</span><span class="sxs-lookup"><span data-stu-id="9541f-104">Text</span></span>

<span data-ttu-id="9541f-105">O nome do elemento ( {0} ) não deve conter o texto da função do elemento ( {1} )</span><span class="sxs-lookup"><span data-stu-id="9541f-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="9541f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9541f-106">Type</span></span>

<span data-ttu-id="9541f-107">Aviso</span><span class="sxs-lookup"><span data-stu-id="9541f-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="9541f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9541f-108">Description</span></span>

<span data-ttu-id="9541f-109">O nome de um elemento incorpora sua função de MSAA ou tipo de controle UIA.</span><span class="sxs-lookup"><span data-stu-id="9541f-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="9541f-110">Por exemplo, esse aviso pode ocorrer se o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) — que é usado para recuperar o nome de MSAA de um elemento — retorna " \_ barra de rolagem do sistema de função \_ \_ \* ".</span><span class="sxs-lookup"><span data-stu-id="9541f-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="9541f-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque a função será lida duas vezes, ou pode ser inpronunciada ou não intuitiva para os usuários.</span><span class="sxs-lookup"><span data-stu-id="9541f-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9541f-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="9541f-112">Possible causes</span></span>

-   <span data-ttu-id="9541f-113">O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="9541f-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="9541f-114">O elemento ou seu pai tem um nome padrão que não foi revisado para um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="9541f-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="9541f-115">Por exemplo, Button1.</span><span class="sxs-lookup"><span data-stu-id="9541f-115">For example, button1.</span></span>
-   <span data-ttu-id="9541f-116">Um desenvolvedor não está ciente de que os leitores de tela lêem nomes.</span><span class="sxs-lookup"><span data-stu-id="9541f-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9541f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9541f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9541f-118">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="9541f-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="9541f-119">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="9541f-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




