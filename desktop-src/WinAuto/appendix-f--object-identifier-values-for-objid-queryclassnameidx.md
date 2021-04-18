---
title: Apêndice F valores de identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Quando OLEACC envia uma \_ mensagem do WM GetObject com o parâmetro lParam definido como OBJIDQUERYCLASSNAMEIDX, muitos usuários padrão ou controles comuns (COMCTL) retornam um dos valores a seguir.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810731"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="3046b-103">Apêndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX</span><span class="sxs-lookup"><span data-stu-id="3046b-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="3046b-104">Quando OLEACC envia uma mensagem do [**WM \_ GetObject**](wm-getobject.md) com o parâmetro *lParam* definido como OBJIDQUERYCLASSNAMEIDX, muitos usuários padrão ou controles comuns (COMCTL) retornam um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3046b-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="3046b-105">USUÁRIO ou controle comum</span><span class="sxs-lookup"><span data-stu-id="3046b-105">USER or common control</span></span> | <span data-ttu-id="3046b-106">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3046b-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="3046b-107">Caixas</span><span class="sxs-lookup"><span data-stu-id="3046b-107">Listbox</span></span>                | <span data-ttu-id="3046b-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="3046b-108">65536+0</span></span>      |
| <span data-ttu-id="3046b-109">Botão</span><span class="sxs-lookup"><span data-stu-id="3046b-109">Button</span></span>                 | <span data-ttu-id="3046b-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="3046b-110">65536+2</span></span>      |
| <span data-ttu-id="3046b-111">Estático</span><span class="sxs-lookup"><span data-stu-id="3046b-111">Static</span></span>                 | <span data-ttu-id="3046b-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="3046b-112">65536+3</span></span>      |
| <span data-ttu-id="3046b-113">Editar</span><span class="sxs-lookup"><span data-stu-id="3046b-113">Edit</span></span>                   | <span data-ttu-id="3046b-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="3046b-114">65536+4</span></span>      |
| <span data-ttu-id="3046b-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="3046b-115">Combobox</span></span>               | <span data-ttu-id="3046b-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="3046b-116">65536+5</span></span>      |
| <span data-ttu-id="3046b-117">Rolagem</span><span class="sxs-lookup"><span data-stu-id="3046b-117">Scrollbar</span></span>              | <span data-ttu-id="3046b-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="3046b-118">65536+10</span></span>     |
| <span data-ttu-id="3046b-119">Status</span><span class="sxs-lookup"><span data-stu-id="3046b-119">Status</span></span>                 | <span data-ttu-id="3046b-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="3046b-120">65536+11</span></span>     |
| <span data-ttu-id="3046b-121">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="3046b-121">Toolbar</span></span>                | <span data-ttu-id="3046b-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="3046b-122">65536+12</span></span>     |
| <span data-ttu-id="3046b-123">Progresso</span><span class="sxs-lookup"><span data-stu-id="3046b-123">Progress</span></span>               | <span data-ttu-id="3046b-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="3046b-124">65536+13</span></span>     |
| <span data-ttu-id="3046b-125">Animar</span><span class="sxs-lookup"><span data-stu-id="3046b-125">Animate</span></span>                | <span data-ttu-id="3046b-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="3046b-126">65536+14</span></span>     |
| <span data-ttu-id="3046b-127">Tab</span><span class="sxs-lookup"><span data-stu-id="3046b-127">Tab</span></span>                    | <span data-ttu-id="3046b-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="3046b-128">65536+15</span></span>     |
| <span data-ttu-id="3046b-129">Tecla de acesso</span><span class="sxs-lookup"><span data-stu-id="3046b-129">Hotkey</span></span>                 | <span data-ttu-id="3046b-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="3046b-130">65536+16</span></span>     |
| <span data-ttu-id="3046b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3046b-131">Header</span></span>                 | <span data-ttu-id="3046b-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="3046b-132">65536+17</span></span>     |
| <span data-ttu-id="3046b-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="3046b-133">Trackbar</span></span>               | <span data-ttu-id="3046b-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="3046b-134">65536+18</span></span>     |
| <span data-ttu-id="3046b-135">Fotos</span><span class="sxs-lookup"><span data-stu-id="3046b-135">Listview</span></span>               | <span data-ttu-id="3046b-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="3046b-136">65536+19</span></span>     |
| <span data-ttu-id="3046b-137">Updown</span><span class="sxs-lookup"><span data-stu-id="3046b-137">Updown</span></span>                 | <span data-ttu-id="3046b-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="3046b-138">65536+22</span></span>     |
| <span data-ttu-id="3046b-139">Dicas</span><span class="sxs-lookup"><span data-stu-id="3046b-139">ToolTips</span></span>               | <span data-ttu-id="3046b-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="3046b-140">65536+24</span></span>     |
| <span data-ttu-id="3046b-141">TreeView</span><span class="sxs-lookup"><span data-stu-id="3046b-141">Treeview</span></span>               | <span data-ttu-id="3046b-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="3046b-142">65536+25</span></span>     |
| <span data-ttu-id="3046b-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="3046b-143">RichEdit</span></span>               | <span data-ttu-id="3046b-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="3046b-144">65536+28</span></span>     |



 

<span data-ttu-id="3046b-145">Somente o usuário e os COMCTL (controles comuns do Windows) retornarão um dos valores da tabela.</span><span class="sxs-lookup"><span data-stu-id="3046b-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="3046b-146">Se uma janela retornar 0 em resposta a essa mensagem, a janela poderá ser uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="3046b-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="3046b-147">Um controle personalizado</span><span class="sxs-lookup"><span data-stu-id="3046b-147">A custom control</span></span>
-   <span data-ttu-id="3046b-148">Um controle diferente de um dos controles na tabela anterior</span><span class="sxs-lookup"><span data-stu-id="3046b-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="3046b-149">Uma versão antiga de um controle do sistema que não reconhece a mensagem do [**WM \_ GetObject**](wm-getobject.md)</span><span class="sxs-lookup"><span data-stu-id="3046b-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="3046b-150">Se uma janela retornar 0, os clientes talvez precisem usar [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) ou [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span><span class="sxs-lookup"><span data-stu-id="3046b-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="3046b-151">Você pode usar essas funções para determinar o tipo de controle com base no nome da classe.</span><span class="sxs-lookup"><span data-stu-id="3046b-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="3046b-152">Em geral, os clientes podem usar as informações fornecidas pelo OLEACC.</span><span class="sxs-lookup"><span data-stu-id="3046b-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 