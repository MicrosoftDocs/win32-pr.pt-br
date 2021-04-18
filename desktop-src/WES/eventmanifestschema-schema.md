---
title: Esquema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Saiba mais sobre: esquema EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788816"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="61241-103">Esquema EventManifest</span><span class="sxs-lookup"><span data-stu-id="61241-103">EventManifest Schema</span></span>

<span data-ttu-id="61241-104">O esquema EventManifest define os seguintes elementos e tipos que você usa para escrever um manifesto de instrumentação:</span><span class="sxs-lookup"><span data-stu-id="61241-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="61241-105">Elementos EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="61241-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="61241-106">Tipos simples de EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="61241-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="61241-107">Tipos complexos EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="61241-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="61241-108">A seção elementos contém os nomes dos elementos que você usa em seu manifesto; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.</span><span class="sxs-lookup"><span data-stu-id="61241-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="61241-109">Um manifesto de instrumentação é um arquivo XML que define um provedor de eventos, os canais nos quais os eventos são gravados, os próprios eventos, os critérios de filtragem de eventos, como níveis, tarefas e opcodes, e as cadeias de caracteres localizadas usadas ao renderizar os eventos.</span><span class="sxs-lookup"><span data-stu-id="61241-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="61241-110">A Convenção é usar. Man como a extensão para arquivos de manifesto.</span><span class="sxs-lookup"><span data-stu-id="61241-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="61241-111">Para obter detalhes sobre como escrever um manifesto, consulte [escrevendo um manifesto de instrumentação](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="61241-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="61241-112">O SDK do Windows inclui o esquema no \\ arquivo de \\ evento. xsd de inclusão.</span><span class="sxs-lookup"><span data-stu-id="61241-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="61241-113">Você pode usar o XSD para validar seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="61241-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="61241-114">Além do esquema EventManifest, o log de eventos do Windows também define os seguintes esquemas:</span><span class="sxs-lookup"><span data-stu-id="61241-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="61241-115">[Esquema de evento](eventschema-schema.md)— define os elementos e tipos usados para renderizar um evento.</span><span class="sxs-lookup"><span data-stu-id="61241-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="61241-116">[Esquema de consulta](queryschema-schema.md)— define os elementos e tipos usados para gravar uma consulta para recuperar eventos de um ou mais canais.</span><span class="sxs-lookup"><span data-stu-id="61241-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




