---
description: Um DC (contexto de dispositivo) é uma estrutura de dados que define os objetos gráficos, seus atributos associados e os modos gráficos que afetam a saída em um dispositivo. Para criar um controlador de domínio, chame a função CreateDC; para recuperar um controlador de domínio, chame a função GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmaps, contextos de dispositivo e superfícies de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165093"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="eaa98-104">Bitmaps, contextos de dispositivo e superfícies de desenho</span><span class="sxs-lookup"><span data-stu-id="eaa98-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="eaa98-105">Um DC ( *contexto de dispositivo* ) é uma estrutura de dados que define os objetos gráficos, seus atributos associados e os modos gráficos que afetam a saída em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eaa98-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="eaa98-106">Para criar um controlador de domínio, chame a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ; para recuperar um controlador de domínio, chame a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="eaa98-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="eaa98-107">Antes de retornar um identificador que identifica esse DC, o sistema seleciona uma superfície de desenho no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="eaa98-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="eaa98-108">Se o aplicativo chamou a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) para criar um contexto de dispositivo para uma exibição VGA, as dimensões dessa superfície de desenho serão de 640 a 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="eaa98-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="eaa98-109">Se o aplicativo tiver chamado a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , as dimensões refletirão o tamanho da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="eaa98-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="eaa98-110">Antes que um aplicativo possa começar a desenhar, ele deve selecionar um bitmap com a largura e a altura apropriadas no controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="eaa98-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="eaa98-111">Quando um aplicativo passa o identificador para o controlador de domínio para uma das funções de desenho da interface de dispositivo de gráficos (GDI), a saída solicitada aparece na superfície de desenho selecionada no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="eaa98-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="eaa98-112">Para obter mais informações, consulte [contextos de dispositivo de memória](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="eaa98-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



