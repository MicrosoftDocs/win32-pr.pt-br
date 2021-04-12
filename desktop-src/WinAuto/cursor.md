---
title: Cursor (referência de elemento de interface do usuário MSAA)
description: Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball. Quando o usuário move o dispositivo apontador, o sistema operacional Windows move o cursor.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291902"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="7a2d2-104">Cursor (referência de elemento de interface do usuário MSAA)</span><span class="sxs-lookup"><span data-stu-id="7a2d2-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="7a2d2-105">Este tópico descreve os cursores para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="7a2d2-106">Como usar cursores em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="7a2d2-107">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="7a2d2-108">Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="7a2d2-109">Quando o usuário move o dispositivo apontador, o sistema operacional Windows move o cursor.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="7a2d2-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="7a2d2-110">IAccessible Methods</span></span>

<span data-ttu-id="7a2d2-111">Um cursor dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="7a2d2-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7a2d2-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7a2d2-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7a2d2-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7a2d2-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="7a2d2-114">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="7a2d2-114">IAccessible Properties</span></span>

<span data-ttu-id="7a2d2-115">Um cursor dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="7a2d2-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="7a2d2-116">[**Get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="7a2d2-117">[**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)– os desenvolvedores podem criar cursores personalizados ou usar os cursores predefinidos que são identificados por sua ID de cursor.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="7a2d2-118">A propriedade **Name** do cursor depende de sua forma e é uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="7a2d2-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="7a2d2-119">Forma do cursor</span><span class="sxs-lookup"><span data-stu-id="7a2d2-119">Cursor shape</span></span>     | <span data-ttu-id="7a2d2-120">Nome</span><span class="sxs-lookup"><span data-stu-id="7a2d2-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="7a2d2-121">Cursor personalizado</span><span class="sxs-lookup"><span data-stu-id="7a2d2-121">Custom cursor</span></span>    | <span data-ttu-id="7a2d2-122">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="7a2d2-122">"Unknown"</span></span>         |
    | <span data-ttu-id="7a2d2-123">seta da IDC \_</span><span class="sxs-lookup"><span data-stu-id="7a2d2-123">IDC\_ARROW</span></span>       | <span data-ttu-id="7a2d2-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-124">"Normal"</span></span>          |
    | <span data-ttu-id="7a2d2-125">\_IBEAM IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="7a2d2-126">Editar</span><span class="sxs-lookup"><span data-stu-id="7a2d2-126">"Edit"</span></span>            |
    | <span data-ttu-id="7a2d2-127">espera da IDC \_</span><span class="sxs-lookup"><span data-stu-id="7a2d2-127">IDC\_WAIT</span></span>        | <span data-ttu-id="7a2d2-128">Esperado</span><span class="sxs-lookup"><span data-stu-id="7a2d2-128">"Wait"</span></span>            |
    | <span data-ttu-id="7a2d2-129">\_cruzada da IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-129">IDC\_CROSS</span></span>       | <span data-ttu-id="7a2d2-130">Gráfico</span><span class="sxs-lookup"><span data-stu-id="7a2d2-130">"Graphic"</span></span>         |
    | <span data-ttu-id="7a2d2-131">coseta do IDC \_</span><span class="sxs-lookup"><span data-stu-id="7a2d2-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="7a2d2-132">Limpeza</span><span class="sxs-lookup"><span data-stu-id="7a2d2-132">"Up"</span></span>              |
    | <span data-ttu-id="7a2d2-133">\_SIZENWSE IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="7a2d2-134">"Tamanho do NWSE"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="7a2d2-135">\_SIZENESW IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="7a2d2-136">"Tamanho do NESW"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-136">"NESW size"</span></span>       |
    | <span data-ttu-id="7a2d2-137">\_SIZEWE IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="7a2d2-138">"Tamanho horizontal"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="7a2d2-139">\_SIZENS IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="7a2d2-140">"Tamanho vertical"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="7a2d2-141">\_SIZEALL IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="7a2d2-142">Prosseguir</span><span class="sxs-lookup"><span data-stu-id="7a2d2-142">"Move"</span></span>            |
    | <span data-ttu-id="7a2d2-143">\_n º da IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-143">IDC\_NO</span></span>          | <span data-ttu-id="7a2d2-144">Proibido</span><span class="sxs-lookup"><span data-stu-id="7a2d2-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="7a2d2-145">\_APPSTARTING IDC</span><span class="sxs-lookup"><span data-stu-id="7a2d2-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="7a2d2-146">"Início do aplicativo"</span><span class="sxs-lookup"><span data-stu-id="7a2d2-146">"App start"</span></span>       |
    | <span data-ttu-id="7a2d2-147">ajuda da IDC \_</span><span class="sxs-lookup"><span data-stu-id="7a2d2-147">IDC\_HELP</span></span>        | <span data-ttu-id="7a2d2-148">Podem</span><span class="sxs-lookup"><span data-stu-id="7a2d2-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="7a2d2-149">[**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— a propriedade **role** é [**\_ \_ cursor do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7a2d2-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="7a2d2-150">[**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— a propriedade **State** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):</span><span class="sxs-lookup"><span data-stu-id="7a2d2-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="7a2d2-151">[**Estado \_ sistema \_**](object-state-constants.md) de estado invisível do sistema \| [ **\_ \_ flutuante**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="7a2d2-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="7a2d2-152">Observações</span><span class="sxs-lookup"><span data-stu-id="7a2d2-152">Notes</span></span>

-   <span data-ttu-id="7a2d2-153">Ao contrário de outros elementos da interface do usuário, o objeto de cursor não tem um identificador de janela associado.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="7a2d2-154">Para obter acesso ao objeto cursor, os clientes devem definir um [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e aguardar que o objeto de cursor gere eventos.</span><span class="sxs-lookup"><span data-stu-id="7a2d2-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2d2-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a2d2-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2d2-156">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="7a2d2-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




