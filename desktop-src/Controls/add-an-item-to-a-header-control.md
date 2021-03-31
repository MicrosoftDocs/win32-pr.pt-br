---
title: Como adicionar um item a um controle de cabeçalho
description: Este tópico demonstra como adicionar um item a um controle de cabeçalho.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917806"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="94d8b-103">Como adicionar um item a um controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94d8b-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="94d8b-104">Este tópico demonstra como adicionar um item a um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="94d8b-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="94d8b-105">Um controle de cabeçalho normalmente tem vários itens de cabeçalho que definem as colunas do controle.</span><span class="sxs-lookup"><span data-stu-id="94d8b-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="94d8b-106">Você pode adicionar um item a um controle de cabeçalho enviando a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para o controle.</span><span class="sxs-lookup"><span data-stu-id="94d8b-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="94d8b-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="94d8b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="94d8b-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="94d8b-108">Technologies</span></span>

-   [<span data-ttu-id="94d8b-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="94d8b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="94d8b-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="94d8b-110">Prerequisites</span></span>

-   <span data-ttu-id="94d8b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="94d8b-111">C/C++</span></span>
-   <span data-ttu-id="94d8b-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="94d8b-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="94d8b-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="94d8b-113">Instructions</span></span>


<span data-ttu-id="94d8b-114">Use a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para adicionar um item ao controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="94d8b-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="94d8b-115">A mensagem deve incluir o endereço de uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="94d8b-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="94d8b-116">Essa estrutura define as propriedades do item de cabeçalho, que pode incluir uma cadeia de caracteres, uma imagem de bitmap, um tamanho inicial e um valor de 32 bits definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94d8b-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="94d8b-117">O exemplo a seguir ilustra como usar a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) e a estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) para adicionar um item a um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="94d8b-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="94d8b-118">O novo item consiste em uma cadeia de caracteres que é justificada à esquerda dentro do retângulo do item.</span><span class="sxs-lookup"><span data-stu-id="94d8b-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="94d8b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94d8b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94d8b-120">Sobre controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94d8b-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="94d8b-121">Referência de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94d8b-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="94d8b-122">Usando controles de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94d8b-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




