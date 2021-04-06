---
title: Como dar suporte a itens de retorno de chamada
description: Este tópico demonstra como fornecer suporte para itens de retorno de chamada.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917791"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="7c1e1-103">Como dar suporte a itens de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="7c1e1-103">How to Support Callback Items</span></span>

<span data-ttu-id="7c1e1-104">Este tópico demonstra como fornecer suporte para itens de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7c1e1-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7c1e1-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="7c1e1-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7c1e1-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="7c1e1-106">Technologies</span></span>

-   [<span data-ttu-id="7c1e1-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1e1-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7c1e1-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7c1e1-108">Prerequisites</span></span>

-   <span data-ttu-id="7c1e1-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7c1e1-109">C/C++</span></span>
-   <span data-ttu-id="7c1e1-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1e1-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7c1e1-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="7c1e1-111">Instructions</span></span>


<span data-ttu-id="7c1e1-112">Se seu aplicativo for usar itens de retorno de chamada em um controle ComboBoxEx, ele deverá estar preparado para lidar com o código de notificação [ \_ GETDISPINFO do CBEN](cben-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1e1-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="7c1e1-113">Um controle ComboBoxEx envia essa notificação sempre que precisa do proprietário para fornecer informações de item específicas.</span><span class="sxs-lookup"><span data-stu-id="7c1e1-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="7c1e1-114">Para obter mais informações sobre itens de retorno de chamada, consulte [itens de retorno de chamada](comboboxex-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e1-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="7c1e1-115">A função definida pelo aplicativo a seguir processa [CBEN \_ GETDISPINFO](cben-getdispinfo.md) fornecendo atributos para um determinado item.</span><span class="sxs-lookup"><span data-stu-id="7c1e1-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="7c1e1-116">Observe que ele define o membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de entrada para CBEIF \_ di \_ SETITEM.</span><span class="sxs-lookup"><span data-stu-id="7c1e1-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="7c1e1-117">A definição de **Mask** para esse valor faz com que o controle retenha as informações do item para que não seja necessário solicitar as informações novamente.</span><span class="sxs-lookup"><span data-stu-id="7c1e1-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="7c1e1-118">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="7c1e1-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="7c1e1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c1e1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c1e1-120">Sobre controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7c1e1-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="7c1e1-121">Referência de controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7c1e1-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7c1e1-122">Usando controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7c1e1-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="7c1e1-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7c1e1-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 