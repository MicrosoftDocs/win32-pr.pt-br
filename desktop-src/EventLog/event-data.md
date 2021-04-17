---
description: Cada evento pode ter dados específicos de eventos associados a ele.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Dados de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770420"
---
# <a name="event-data"></a><span data-ttu-id="82c86-103">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="82c86-103">Event Data</span></span>

<span data-ttu-id="82c86-104">Cada evento pode ter dados específicos de eventos associados a ele.</span><span class="sxs-lookup"><span data-stu-id="82c86-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="82c86-105">O Visualizador de Eventos não interpreta esses dados; Ele exibe dados adicionais somente em um formato hexadecimal e de texto combinado.</span><span class="sxs-lookup"><span data-stu-id="82c86-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="82c86-106">O limite máximo do tamanho de um evento no log par é de 0x3FFFF bytes.</span><span class="sxs-lookup"><span data-stu-id="82c86-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="82c86-107">Portanto, use dados específicos de eventos com moderação, incluindo-os somente se você tiver certeza de que será útil para alguém que esteja Depurando um problema.</span><span class="sxs-lookup"><span data-stu-id="82c86-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="82c86-108">Por exemplo, muitos eventos relacionados à rede incluem o NCB (blocos de controle de rede) como dados específicos de eventos.</span><span class="sxs-lookup"><span data-stu-id="82c86-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="82c86-109">Quando você usa dados específicos do evento, a última parte de sua cadeia de caracteres de descrição deve fornecer uma observação sobre as informações fornecidas como dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="82c86-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="82c86-110">Por exemplo, o software de rede pode fornecer uma observação como: "(o NCB são os dados de evento.)" Como uma convenção, use parênteses em relação a tais comentários, conforme indicado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="82c86-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="82c86-111">Você também pode usar dados específicos de eventos para armazenar informações que o aplicativo pode processar independentemente do Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="82c86-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="82c86-112">Por exemplo, você pode escrever um visualizador especificamente para seus eventos ou escrever um programa que examina o log e cria um relatório que inclui informações dos dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="82c86-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 



