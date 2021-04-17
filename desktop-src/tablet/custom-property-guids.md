---
description: Os seguintes identificadores globalmente exclusivos (GUIDs) são usados pelo diário do Windows para identificar Propriedades personalizadas em traçados ou atributos de desenho.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUIDs de propriedade personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790465"
---
# <a name="custom-property-guids"></a><span data-ttu-id="eb211-103">GUIDs de propriedade personalizada</span><span class="sxs-lookup"><span data-stu-id="eb211-103">Custom Property GUIDs</span></span>

<span data-ttu-id="eb211-104">Os seguintes identificadores globalmente exclusivos (GUIDs) são usados pelo diário do Windows para identificar Propriedades personalizadas em traçados ou atributos de desenho.</span><span class="sxs-lookup"><span data-stu-id="eb211-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="eb211-105">\_carimbo de \_ data/hora de traço GUID</span><span class="sxs-lookup"><span data-stu-id="eb211-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="eb211-106">Essa é uma estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) que indica a hora em que o traço foi criado ou adicionado ao documento.</span><span class="sxs-lookup"><span data-stu-id="eb211-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="eb211-107">\_hora de corte do GUID \_</span><span class="sxs-lookup"><span data-stu-id="eb211-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="eb211-108">Esta é uma estrutura de **TimeID** .</span><span class="sxs-lookup"><span data-stu-id="eb211-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="eb211-109">Ele permite que a ordem dos traços seja mantida nas operações de colar e soltar.</span><span class="sxs-lookup"><span data-stu-id="eb211-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="eb211-110">Sem a estrutura de **TimeID** , o carimbo de data/hora para todos os objetos da [**interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recortados e colados em uma [coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="eb211-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="eb211-111">realce de GUID \_</span><span class="sxs-lookup"><span data-stu-id="eb211-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="eb211-112">É um **bool**, em que **true**= Ink do realçador, **false**= Ink regular.</span><span class="sxs-lookup"><span data-stu-id="eb211-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="eb211-113">Isso é aplicado aos atributos de desenho.</span><span class="sxs-lookup"><span data-stu-id="eb211-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="eb211-114">estilo de tinta de GUID em \_ \_ \_ negrito</span><span class="sxs-lookup"><span data-stu-id="eb211-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="eb211-115">É um **bool**, onde **true**= Ink negrito, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="eb211-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="eb211-116">Isso é aplicado aos atributos de desenho.</span><span class="sxs-lookup"><span data-stu-id="eb211-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="eb211-117">\_itálico do \_ estilo de tinta do GUID \_</span><span class="sxs-lookup"><span data-stu-id="eb211-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="eb211-118">É um **bool**, onde **true**= Ink em itálico, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="eb211-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="eb211-119">Isso é aplicado aos atributos de desenho.</span><span class="sxs-lookup"><span data-stu-id="eb211-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="eb211-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb211-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb211-121">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="eb211-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
