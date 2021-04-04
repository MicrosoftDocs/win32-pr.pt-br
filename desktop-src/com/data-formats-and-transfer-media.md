---
title: Formatos de dados e mídia de transferência
description: Formatos de dados e mídia de transferência
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104008587"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="d9317-103">Formatos de dados e mídia de transferência</span><span class="sxs-lookup"><span data-stu-id="d9317-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="d9317-104">A maioria das plataformas, incluindo o Windows, define um protocolo padrão para transferir dados entre aplicativos, com base em um conjunto de funções chamado de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="d9317-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="d9317-105">Os aplicativos que usam essas funções podem compartilhar dados mesmo que seus formatos de dados nativos sejam indiferentemente diferentes.</span><span class="sxs-lookup"><span data-stu-id="d9317-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="d9317-106">Em geral, essas áreas de transferência têm duas falhas significativas que o COM supera.</span><span class="sxs-lookup"><span data-stu-id="d9317-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="d9317-107">Primeiro, as descrições de dados usam apenas um identificador de formato, como o identificador de formato de área de transferência de 16 bits único no Windows, o que significa que a área de transferência só pode descrever a estrutura de seus dados, ou seja, a ordem dos bits.</span><span class="sxs-lookup"><span data-stu-id="d9317-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="d9317-108">Ele pode relatar, "tenho um bitmap" "ou ter algum texto," mas não pode especificar os dispositivos de destino para os quais os dados são compostos, quais modos de exibição ou aspectos de si mesmos os dados podem fornecer, ou quais mídias de armazenamento são mais adequadas para sua transferência.</span><span class="sxs-lookup"><span data-stu-id="d9317-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="d9317-109">Por exemplo, ele não pode relatar: "tenho uma cadeia de texto que é armazenada na memória global e formatada para apresentação na tela ou em uma impressora" ou "tenho um bitmap de esboço em miniatura renderizado para uma impressora matricial de ponto de 100 dpi e armazenado como um arquivo de disco".</span><span class="sxs-lookup"><span data-stu-id="d9317-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="d9317-110">Em segundo lugar, todas as transferências de dados que usam a área de transferência geralmente ocorrem por meio da memória global.</span><span class="sxs-lookup"><span data-stu-id="d9317-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="d9317-111">O uso da memória global é razoavelmente eficiente para pequenas quantidades de dados, mas terrivelmente ineficiente para grandes quantidades, como um objeto multimídia de 20 MB.</span><span class="sxs-lookup"><span data-stu-id="d9317-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="d9317-112">A memória global está lenta para um objeto de dados grande, cujo tamanho requer uma troca considerável na memória virtual no disco.</span><span class="sxs-lookup"><span data-stu-id="d9317-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="d9317-113">Nos casos em que os dados que estão sendo trocados vão residir principalmente no disco de qualquer forma, forçá-lo por meio desse afunilamento de memória virtual é altamente ineficiente.</span><span class="sxs-lookup"><span data-stu-id="d9317-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="d9317-114">Uma maneira melhor seria ignorar totalmente a memória global e simplesmente transferir os dados diretamente para o disco.</span><span class="sxs-lookup"><span data-stu-id="d9317-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="d9317-115">Para aliviar esses problemas, o COM fornece duas estruturas de dados: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="d9317-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="d9317-116">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d9317-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d9317-117">A estrutura FORMATETC</span><span class="sxs-lookup"><span data-stu-id="d9317-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="d9317-118">A estrutura STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="d9317-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="d9317-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9317-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9317-120">Transferência de Dados</span><span class="sxs-lookup"><span data-stu-id="d9317-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




