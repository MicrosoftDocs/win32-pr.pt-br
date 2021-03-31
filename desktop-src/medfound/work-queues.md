---
description: No Microsoft Media Foundation, uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Filas de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169752"
---
# <a name="work-queues"></a><span data-ttu-id="e74f3-103">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="e74f3-103">Work Queues</span></span>

<span data-ttu-id="e74f3-104">No Microsoft Media Foundation, uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread.</span><span class="sxs-lookup"><span data-stu-id="e74f3-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="e74f3-105">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="e74f3-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e74f3-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="e74f3-106">Topic</span></span></th>
<th><span data-ttu-id="e74f3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e74f3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e74f3-108"><a href="using-work-queues.md">Usando filas de trabalho</a></span><span class="sxs-lookup"><span data-stu-id="e74f3-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="e74f3-109">Descreve como um aplicativo ou componente pode usar filas de trabalho para executar operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="e74f3-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e74f3-110"><a href="writing-an-asynchronous-method.md">Escrevendo um método assíncrono</a></span><span class="sxs-lookup"><span data-stu-id="e74f3-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="e74f3-111">Descreve como escrever um método assíncrono que segue o padrão de início/término descrito em <a href="asynchronous-callback-methods.md">métodos de retorno de chamada assíncronos</a>.</span><span class="sxs-lookup"><span data-stu-id="e74f3-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e74f3-112"><a href="custom-asynchronous-result-objects.md">Objetos de resultados assíncronos personalizados</a></span><span class="sxs-lookup"><span data-stu-id="e74f3-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="e74f3-113">Descreve como criar uma implementação personalizada da interface <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e74f3-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e74f3-114">A maioria dos aplicativos deve usar a implementação de estoque fornecida pelo <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e74f3-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="e74f3-115">Este tópico é para aplicativos com requisitos avançados.</span><span class="sxs-lookup"><span data-stu-id="e74f3-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e74f3-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Aprimoramentos na fila de trabalho e threading</a></span><span class="sxs-lookup"><span data-stu-id="e74f3-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="e74f3-117">Descreve melhorias no Windows 8 para filas de trabalho e threading na plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e74f3-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e74f3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e74f3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74f3-119">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e74f3-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




