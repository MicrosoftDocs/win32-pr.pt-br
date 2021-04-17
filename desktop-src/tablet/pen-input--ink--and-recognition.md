---
description: Um novo recurso interessante do Tablet PC é o sistema de entrada de caneta.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrada, tinta e reconhecimento de caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567636"
---
# <a name="pen-input-ink-and-recognition"></a><span data-ttu-id="f2e93-103">Entrada, tinta e reconhecimento de caneta</span><span class="sxs-lookup"><span data-stu-id="f2e93-103">Pen Input, Ink, and Recognition</span></span>

<span data-ttu-id="f2e93-104">Um novo recurso interessante do Tablet PC é o sistema de entrada de caneta.</span><span class="sxs-lookup"><span data-stu-id="f2e93-104">One interesting new feature of Tablet PC is the pen input system.</span></span> <span data-ttu-id="f2e93-105">Todos os computadores do Tablet PC têm um digitalizador sob a tela que aceita entrada à caneta.</span><span class="sxs-lookup"><span data-stu-id="f2e93-105">All Tablet PC computers have a digitizer beneath the screen that accepts pen input.</span></span> <span data-ttu-id="f2e93-106">Esse novo mecanismo de entrada exige que você pense em como criar aplicativos especificamente para Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f2e93-106">This new input mechanism requires you to think about how to build applications specifically for Tablet PC.</span></span> <span data-ttu-id="f2e93-107">A API (interface de programação de aplicativo) da plataforma do Tablet PC ajuda você a fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f2e93-107">The Tablet PC platform application programming interface (API) helps you do this.</span></span>

## <a name="collection-data-management-and-recognition"></a><span data-ttu-id="f2e93-108">Coleta, Gerenciamento de Dados e reconhecimento</span><span class="sxs-lookup"><span data-stu-id="f2e93-108">Collection, Data Management, and Recognition</span></span>

<span data-ttu-id="f2e93-109">A plataforma do Tablet PC pode ser dividida em três áreas distintas:</span><span class="sxs-lookup"><span data-stu-id="f2e93-109">The Tablet PC platform can be divided into three distinct areas:</span></span>

-   <span data-ttu-id="f2e93-110">Coleção de tinta (objetos que são usados para coletar tinta do digitalizador).</span><span class="sxs-lookup"><span data-stu-id="f2e93-110">Ink collection (objects that are used to collect ink from the digitizer).</span></span>
-   <span data-ttu-id="f2e93-111">Gerenciamento de dados de tinta (objetos que são usados para gerenciar a tinta coletada).</span><span class="sxs-lookup"><span data-stu-id="f2e93-111">Ink data management (objects that are used to manage the collected ink).</span></span>
-   <span data-ttu-id="f2e93-112">Reconhecimento de tinta (objetos que são usados para converter a tinta coletada em outros tipos de dados, como texto).</span><span class="sxs-lookup"><span data-stu-id="f2e93-112">Ink recognition (objects that are used to convert the collected ink into other types of data, such as text).</span></span>

<span data-ttu-id="f2e93-113">A imagem a seguir mostra, em um alto nível, como a API de coleta de tinta (API de caneta), a API de Gerenciamento de Dados de tinta (API de tinta) e a API de reconhecimento de tinta (API de reconhecimento) funcionam juntas na plataforma do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f2e93-113">The following image shows, at a high level, how the Ink Collection API (Pen API), Ink Data Management API (Ink API), and Ink Recognition API (Recognition API) work together in the Tablet PC platform.</span></span>

![ilustração mostrando como a API de caneta, a API de tinta e a API de reconhecimento funcionam juntas](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

<span data-ttu-id="f2e93-115">A API da plataforma do Tablet PC está disponível em APIs gerenciadas, bem como em uma biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="f2e93-115">The Tablet PC platform API is available in Managed APIs as well as a COM library.</span></span> <span data-ttu-id="f2e93-116">Os tópicos a seguir descrevem os objetos na API e ilustram como os aplicativos usam esses objetos:</span><span class="sxs-lookup"><span data-stu-id="f2e93-116">The following topics describe the objects in the API and illustrate how applications use these objects:</span></span>

-   [<span data-ttu-id="f2e93-117">Coleta de tinta</span><span class="sxs-lookup"><span data-stu-id="f2e93-117">Ink Collection</span></span>](ink-collection.md)
-   [<span data-ttu-id="f2e93-118">Dados de tinta</span><span class="sxs-lookup"><span data-stu-id="f2e93-118">Ink Data</span></span>](ink-data.md)
-   [<span data-ttu-id="f2e93-119">Reconhecimento de tinta</span><span class="sxs-lookup"><span data-stu-id="f2e93-119">Ink Recognition</span></span>](ink-recognition.md)
-   [<span data-ttu-id="f2e93-120">Análise de tinta</span><span class="sxs-lookup"><span data-stu-id="f2e93-120">Ink Analysis</span></span>](ink-analysis.md)
-   [<span data-ttu-id="f2e93-121">Reconhecimento de manuscrito no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2e93-121">Handwriting Recognition in Windows Server 2008 R2</span></span>](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



