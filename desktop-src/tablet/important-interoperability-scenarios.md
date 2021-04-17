---
description: 'Para que um aplicativo de Tablet PC opere com tinta com eficiência, esse aplicativo deve ser capaz de:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Cenários importantes de interoperabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749918"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="98709-103">Cenários importantes de interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="98709-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="98709-104">Para que um aplicativo de Tablet PC opere com tinta com eficiência, esse aplicativo deve ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="98709-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="98709-105">Salve um documento no formato binário nativo do aplicativo sem perder a tinta do documento.</span><span class="sxs-lookup"><span data-stu-id="98709-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="98709-106">Salvar um documento em qualquer formato com o qual o aplicativo normalmente dá suporte (por exemplo, HTML ou Rich Text Format (RTF)) sem perder a tinta do documento.</span><span class="sxs-lookup"><span data-stu-id="98709-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="98709-107">Copiar tinta de um aplicativo para outro usando a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="98709-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="98709-108">Isso funcionará se o outro aplicativo reconhecer apenas um formato específico, como HTML, RTF ou bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="98709-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="98709-109">Também funciona se o aplicativo de destino reconhece a tinta.</span><span class="sxs-lookup"><span data-stu-id="98709-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="98709-110">Se ele reconhecer tinta, o aplicativo de destino será capaz de interpretar a tinta que foi copiada como tinta e não apenas como uma imagem.</span><span class="sxs-lookup"><span data-stu-id="98709-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="98709-111">Copiar tinta, juntamente com texto, entre dois aplicativos que reconhecem tinta, cada um com mais de um objeto de [**tinta**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="98709-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="98709-112">Isso requer HTML, RTF ou um formato semelhante.</span><span class="sxs-lookup"><span data-stu-id="98709-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="98709-113">Copiar tinta entre dois aplicativos, cada um deles com um objeto de [**tinta**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="98709-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="98709-114">O ISF (Ink serializado Format) é suficiente para isso.</span><span class="sxs-lookup"><span data-stu-id="98709-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="98709-115">Copie a tinta de um aplicativo que tenha mais de um objeto de [**tinta**](inkdisp-class.md) para um aplicativo que tenha apenas um objeto de **tinta** .</span><span class="sxs-lookup"><span data-stu-id="98709-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="98709-116">Nesse caso, o aplicativo que tem mais de um objeto de **tinta** deve ser capaz de produzir o formato serializado da tinta (ISF).</span><span class="sxs-lookup"><span data-stu-id="98709-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="98709-117">Copie a tinta de um aplicativo que tenha um objeto de [**tinta**](inkdisp-class.md) para um aplicativo que tenha mais de um objeto de **tinta** .</span><span class="sxs-lookup"><span data-stu-id="98709-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="98709-118">Nesse caso, o aplicativo que tem mais de um objeto de **tinta** deve ser capaz de reconhecer ISF.</span><span class="sxs-lookup"><span data-stu-id="98709-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



