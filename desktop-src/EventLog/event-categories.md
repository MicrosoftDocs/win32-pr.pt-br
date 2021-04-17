---
description: As categorias ajudam a organizar eventos para que Visualizador de Eventos possam filtrá-los. Cada fonte de evento pode definir suas próprias categorias numeradas e as cadeias de caracteres de texto para as quais elas estão mapeadas.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorias de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789819"
---
# <a name="event-categories"></a><span data-ttu-id="42a47-104">Categorias de evento</span><span class="sxs-lookup"><span data-stu-id="42a47-104">Event Categories</span></span>

<span data-ttu-id="42a47-105">As categorias ajudam a organizar eventos para que Visualizador de Eventos possam filtrá-los.</span><span class="sxs-lookup"><span data-stu-id="42a47-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="42a47-106">Cada [fonte de evento](event-sources.md) pode definir suas próprias categorias numeradas e as cadeias de caracteres de texto para as quais elas estão mapeadas.</span><span class="sxs-lookup"><span data-stu-id="42a47-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="42a47-107">As categorias devem ser numeradas consecutivamente, começando com o número 1.</span><span class="sxs-lookup"><span data-stu-id="42a47-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="42a47-108">As categorias em si são definidas em um arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="42a47-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="42a47-109">Por exemplo, use a sintaxe a seguir para declarar três categorias de evento.</span><span class="sxs-lookup"><span data-stu-id="42a47-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="42a47-110">No Visualizador de Eventos, os eventos que usam essas categorias terão a categoria 1, categoria 2 ou categoria 3 exibida na coluna **categoria** .</span><span class="sxs-lookup"><span data-stu-id="42a47-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="42a47-111">As categorias podem ser armazenadas em um arquivo de mensagem separado ou em um arquivo que contém mensagens de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="42a47-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="42a47-112">Se você criar um único arquivo de mensagem, certifique-se de que as categorias sejam as primeiras mensagens no arquivo.</span><span class="sxs-lookup"><span data-stu-id="42a47-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="42a47-113">Para obter mais informações sobre como criar e usar arquivos de mensagens, consulte [arquivos de mensagem](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="42a47-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="42a47-114">O número total de categorias é armazenado no valor de **CategoryCount** para a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="42a47-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



