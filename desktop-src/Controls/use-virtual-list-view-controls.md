---
title: Como usar controles de List-View virtual
description: Este tópico demonstra como trabalhar com controles de exibição de lista virtual.
ms.assetid: DA32D7B3-5FDB-4D73-9A72-0D4EEB2A0C4F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3baf5e37d0d4f6da0cdf596dd8ba3c71e852a99
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/08/2021
ms.locfileid: "105762743"
---
# <a name="how-to-use-virtual-list-view-controls"></a><span data-ttu-id="8e0d2-103">Como usar controles de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="8e0d2-103">How to Use Virtual List-View Controls</span></span>

<span data-ttu-id="8e0d2-104">Este tópico demonstra como trabalhar com controles de exibição de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-104">This topic demonstrates how to work with virtual list-view controls.</span></span> <span data-ttu-id="8e0d2-105">Os exemplos de código do C++ que o acompanham mostram como processar mensagens de notificação de controle de exibição de lista virtual, como otimizar o cache e como recuperar um item do cache.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-105">The accompanying C++ code examples show how to process virtual list-view control notification messages, how to optimize the cache, and how to retrieve an item from the cache.</span></span>

-   [<span data-ttu-id="8e0d2-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="8e0d2-106">What you need to know</span></span>](#what-you-need-to-know)
-   [<span data-ttu-id="8e0d2-107">Processar códigos de notificação de controle de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="8e0d2-107">Process Virtual List-View Control Notification Codes</span></span>](#process-virtual-list-view-control-notification-codes)
-   [<span data-ttu-id="8e0d2-108">Otimizar o cache</span><span class="sxs-lookup"><span data-stu-id="8e0d2-108">Optimize the Cache</span></span>](#optimize-the-cache)
-   [<span data-ttu-id="8e0d2-109">Recuperar um item do cache</span><span class="sxs-lookup"><span data-stu-id="8e0d2-109">Retrieve an Item From the Cache</span></span>](#retrieve-an-item-from-the-cache)
-   [<span data-ttu-id="8e0d2-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e0d2-110">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="8e0d2-111">O código de exemplo nesta seção pressupõe que o cache é uma matriz alocada dinamicamente de estruturas definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-111">The example code in this section assumes that the cache is a dynamically allocated array of application-defined structures.</span></span> <span data-ttu-id="8e0d2-112">A estrutura é definida no exemplo de código C++ a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-112">The structure is defined in the following C++ code example.</span></span>

 


```C++
struct RndItem
{
    int   iIcon;                 // Bitmap assigned to this item.
    UINT  state;                 // Item state value.
    TCHAR Title[BUFFER_SIZE];    // BUFFER_SIZE is a user-defined macro value.
    TCHAR SubText1[BUFFER_SIZE]; // Text for the label of the first sub-item.
    TCHAR SubText2[BUFFER_SIZE]; // Text for the label of the second item.
};

```



## <a name="what-you-need-to-know"></a><span data-ttu-id="8e0d2-113">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="8e0d2-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8e0d2-114">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="8e0d2-114">Technologies</span></span>

-   [<span data-ttu-id="8e0d2-115">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="8e0d2-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8e0d2-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8e0d2-116">Prerequisites</span></span>

-   <span data-ttu-id="8e0d2-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="8e0d2-117">C/C++</span></span>
-   <span data-ttu-id="8e0d2-118">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="8e0d2-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8e0d2-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="8e0d2-119">Instructions</span></span>

### <a name="process-virtual-list-view-control-notification-codes"></a><span data-ttu-id="8e0d2-120">Processar códigos de notificação de controle de List-View virtual</span><span class="sxs-lookup"><span data-stu-id="8e0d2-120">Process Virtual List-View Control Notification Codes</span></span>

<span data-ttu-id="8e0d2-121">Além dos códigos de notificação enviados por outros controles de exibição de lista, os controles de exibição de lista virtual também podem enviar os códigos de notificação [LVN \_ ODCACHEHINT](lvn-odcachehint.md) e [**LVN \_ ODFINDITEM**](lvn-odfinditem.md) .</span><span class="sxs-lookup"><span data-stu-id="8e0d2-121">In addition to the notification codes sent by other list-view controls, virtual list-view controls can also send the [LVN\_ODCACHEHINT](lvn-odcachehint.md) and [**LVN\_ODFINDITEM**](lvn-odfinditem.md) notification codes.</span></span>

<span data-ttu-id="8e0d2-122">Essa função definida pelo aplicativo manipula mensagens de notificação que normalmente são enviadas de um controle de exibição de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-122">This application-defined function handles notification messages that are commonly sent from a virtual list-view control.</span></span>


```C++
LRESULT OnNotify(HWND hwnd, NMHDR* pnmhdr)
{
    HRESULT hr;
    LRESULT lrt = FALSE;

    switch (pnmhdr->code)
    {
    case LVN_GETDISPINFO:
        {
            RndItem rndItem;
            NMLVDISPINFO* plvdi = (NMLVDISPINFO*) pnmhdr;

            if (-1 == plvdi->item.iItem)
            {
                OutputDebugString(TEXT("LVOWNER: Request for -1 item?\n"));
                DebugBreak();
            }

            // Retrieve information for item at index iItem.
            RetrieveItem( &rndItem, plvdi->item.iItem );

            if(plvdi->item.mask & LVIF_STATE)
            {
                // Fill in the state information.
                plvdi->item.state |= rndItem.state;
            }

            if(plvdi->item.mask & LVIF_IMAGE)
            {
                // Fill in the image information.
                plvdi->item.iImage = rndItem.iIcon;
            }

            if(plvdi->item.mask & LVIF_TEXT)
            {
                // Fill in the text information.
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // Copy the main item text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.Title);

                    if(FAILED(hr))
                    { 
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                                
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated.
                    }
                    break;

                case 1:
                    // Copy SubItem1 text.
                    hr = StringCchCopy( plvdi->item.pszText, MAX_COUNT, rndItem.SubText1);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter               
                        // more characters than specified by MAX_COUNT or   
                        // the text will be truncated..
                    }
                    break;

                case 2:
                    // Copy SubItem2 text.
                    hr = StringCchCopy(plvdi->item.pszText, MAX_COUNT, rndItem.SubText2);

                    if(FAILED(hr))
                    {
                        // Insert error handling code here. MAX_COUNT
                        // is a user-defined value. You must not enter                    
                        // more characters than specified by MAX_COUNT or  
                        // the text will be truncated..
                    }
                    break;

                default:
                    break;

                }

            }

            lrt = FALSE;
            break;
        }

    case LVN_ODCACHEHINT:
        {
            NMLVCACHEHINT* pcachehint = (NMLVCACHEHINT*) pnmhdr;

            // Load the cache with the recommended range.
            PrepCache( pcachehint->iFrom, pcachehint->iTo );
            break;
        }

    case LVN_ODFINDITEM:
        {
            LPNMLVFINDITEM pnmfi = NULL;
            
            pnmfi = (LPNMLVFINDITEM)pnmhdr;

            // Call a user-defined function that finds the index according to
            // LVFINDINFO (which is embedded in the LPNMLVFINDITEM structure).
            // If nothing is found, then set the return value to -1.

            break;
        }

    default:
        break;

    }       // End Switch block.

    return(lrt);
}
```



### <a name="optimize-the-cache"></a><span data-ttu-id="8e0d2-123">Otimizar o cache</span><span class="sxs-lookup"><span data-stu-id="8e0d2-123">Optimize the Cache</span></span>

<span data-ttu-id="8e0d2-124">Um controle de exibição de lista virtual envia uma mensagem de notificação [LVN \_ ODCACHEHINT](lvn-odcachehint.md) quando o conteúdo de sua área de exibição é alterado.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-124">A virtual list-view control sends a [LVN\_ODCACHEHINT](lvn-odcachehint.md) notification message when the contents of its display area have changed.</span></span> <span data-ttu-id="8e0d2-125">A mensagem contém informações sobre o intervalo de itens a serem armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-125">The message contains information about the range of items to be cached.</span></span> <span data-ttu-id="8e0d2-126">Ao receber a mensagem de notificação, seu aplicativo deve estar preparado para carregar o cache com informações de item para o intervalo solicitado para que as informações estejam prontamente disponíveis quando uma mensagem de notificação [LVN \_ GETDISPINFO](lvn-getdispinfo.md) for enviada.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-126">Upon receiving the notification message, your application must be prepared to load the cache with item information for the requested range so that the information will be readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification message is sent.</span></span>

<span data-ttu-id="8e0d2-127">No exemplo de código C++ a seguir, a função definida pelo aplicativo aceita o intervalo de itens para o cache Enviado por um controle de exibição de lista virtual.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-127">In the following C++ code example, the application-defined function accepts the range of items for the cache that is sent by a virtual list-view control.</span></span> <span data-ttu-id="8e0d2-128">Ele executa uma verificação para determinar que o intervalo solicitado de itens ainda não está em cache e, em seguida, aloca a memória global necessária e preenche o cache, se necessário.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-128">It performs a verification to determine that the requested range of items is not already cached, and then it allocates the required global memory and fills the cache if necessary.</span></span>


```C++
void PrepCache(int iFrom, int iTo)
{
    /*  Global Variables

     *  g_priCache[ ]: the main cache.
     *  g_iCache:      the index of the first item in the main cache.
     *  g_cCache:      the count of items in the main cache.
     *
     *  g_priEndCache[ ]: the cache of items at the end of the list.
     *  g_iEndCache:      the index of the first item in the end cache.
     *  g_cEndCache:      the count of items in the end cache.
     */
     
    // Local Variables
    int i;
    BOOL fOLFrom = FALSE;
    BOOL   fOLTo = FALSE;

    // Check to see if this is the end cache.
    if ((iTo == g_cCache - 1) && ((iTo - iFrom) < 30))  // 30 entries wide.
    {
        // Check to see if this is a portion of the current end cache.
        if ((g_cCache) && (iFrom >= g_iEndCache) && (iFrom < g_iEndCache+g_cEndCache))
            return;
            // If it is a part of current end cache, no loading is necessary.

        // This is a new end cache. Free the old memory.
        if ( g_priEndCache )
            GlobalFree( g_priEndCache );
            
        // Set the index and count values for the new end cache,
        // and then retrieve the memory.
        g_iEndCache   = iFrom;
        g_cEndCache   = (iTo - iFrom + 1);
        g_priEndCache = (RndItem *)GlobalAlloc(GPTR, sizeof(RndItem) * g_cEndCache);

        if (! g_priEndCache)
        {
            // TODO: Out of memory. Perform error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cEndCache; i++)
        {
            // TODO: Call a function that accesses item information and
            // fills a cache element.
        }
    }

    else
    {   
        // It is not a member of the current end cache.
        // Try the primary cache instead.

        // Check to see if iFrom is within the primary cache.
        if ((g_cCache) && (iFrom >= g_iCache) && (iFrom < g_iCache+g_cCache))
            fOLFrom = TRUE;

        // Check to see if iTo is within the primary cache.
        if ((g_cCache) && (iTo >= g_iCache) && (iTo <= g_iCache+g_cCache))
            fOLTo = TRUE;

        // do nothing if both iFrom and iTo are within the current cache.

        if (fOLFrom && fOLTo)
            return;

        // Enlarge the cache size rather than make it specific to this hint.
        if (fOLFrom)
            iFrom = g_iCache;

        else if (fOLTo)
            iTo = g_iCache + g_cCache;

        // A new primary cache is needed. Free the old primary cache.
        if ( g_priCache )
            GlobalFree( g_priCache );

        // Set the index and count values for the new primary cache,
        // and then retrieve the memory.
        g_iCache   = iFrom;
        g_cCache   = (iTo - iFrom + 1);
        g_priCache = (RndItem *)GlobalAlloc( GPTR, sizeof( RndItem ) * g_cCache );

        if (!g_priCache)
        {
            // TODO: Out of memory. Do error handling.
        }

        // Loop to fill the cache with the recommended items.
        for (i=0; i<g_cCache; i++)
        {
            // TODO: Call a function that accesses item information
            // and fills a cache element.
        }
    }
}
```



### <a name="retrieve-an-item-from-the-cache"></a><span data-ttu-id="8e0d2-129">Recuperar um item do cache</span><span class="sxs-lookup"><span data-stu-id="8e0d2-129">Retrieve an Item From the Cache</span></span>

<span data-ttu-id="8e0d2-130">Essa função de exemplo aceita dois parâmetros, o endereço da estrutura definida pelo aplicativo e um valor inteiro que representa o índice do item na lista.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-130">This example function accepts two parameters, the address of the application-defined structure and an integer value representing the index of the item in the list.</span></span> <span data-ttu-id="8e0d2-131">Ele verifica o valor de índice para descobrir se o item desejado está armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-131">It checks the index value to discover if the desired item is cached.</span></span> <span data-ttu-id="8e0d2-132">Se for, o ponteiro passado para a função será definido como um local no cache.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-132">If it is, the pointer that was passed to the function is set to a location in the cache.</span></span> <span data-ttu-id="8e0d2-133">Se o item não estiver no cache principal ou final, as informações do item deverão ser localizadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e0d2-133">If the item is not in the main or end cache, the item information must be located manually.</span></span>


```C++
void RetrieveItem( RndItem * prndItem, int index )
{
    // Global Variables

    // g_priCache[ ]: the main cache.
    // g_iCache:      the index of the first item in the main cache.
    // c_cCache:      the count of items in the main cache.
    //
    // g_priEndCache[ ]:  the cache of items at the end of the list.
    // g_iEndCache:       the index of the first item in the end cache.
    // g_cEndCache:       the count of items in the end cache.
    //

    // Check to see if the item is in the main cache.
    if ((index >= g_iCache) && (index < g_iCache + g_cCache))
        *prndItem = g_priCache[index-g_iCache];

    // If it is not in the main cache, then check to see if
    // the item is in the end area cache.
    else if ((index >= g_iEndCache) && (index < g_iEndCache + g_cEndCache))
        *prndItem = g_priEndCache[index-g_iEndCache];

    else
    {
        // The item is not in either cache.
        // Therefore, retrieve the item information manually.
    }
}
```



## <a name="remarks"></a><span data-ttu-id="8e0d2-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e0d2-134">Remarks</span></span>

<span data-ttu-id="8e0d2-135">Para obter uma lista das mensagens de janela processadas por um controle de exibição de lista, consulte [padrão List-View processamento de mensagens](listview-message-processing.md).</span><span class="sxs-lookup"><span data-stu-id="8e0d2-135">For a list of the window messages processed by a list-view control, see [Default List-View Message Processing](listview-message-processing.md).</span></span>

## <a name="complete-example"></a><span data-ttu-id="8e0d2-136">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="8e0d2-136">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e0d2-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e0d2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e0d2-138">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="8e0d2-138">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8e0d2-139">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="8e0d2-139">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="8e0d2-140">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="8e0d2-140">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




