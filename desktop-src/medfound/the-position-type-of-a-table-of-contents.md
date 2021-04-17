---
description: O tipo de posição de um sumário
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: O tipo de posição de um sumário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813348"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="c875c-103">O tipo de posição de um sumário</span><span class="sxs-lookup"><span data-stu-id="c875c-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="c875c-104">Alguns métodos da interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) têm um parâmetro chamado *enumTocPosType* que tem um tipo de [**tipo de PDV de Sumário de enumeração \_ \_**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span><span class="sxs-lookup"><span data-stu-id="c875c-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="c875c-105">Esse parâmetro especifica a posição em um arquivo de mídia em que um sumário é armazenado.</span><span class="sxs-lookup"><span data-stu-id="c875c-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="c875c-106">A intenção era que o Sumário pudesse ser armazenado no cabeçalho do arquivo ou no corpo do arquivo como um objeto de nível superior.</span><span class="sxs-lookup"><span data-stu-id="c875c-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="c875c-107">Essa funcionalidade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="c875c-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="c875c-108">Atualmente, as tabelas de conteúdo só podem ser armazenadas como objetos de nível superior, portanto, você deve sempre definir o parâmetro *enumTocPosType* como **TOC \_ \_ TOPLEVELOBJECT do PDV**.</span><span class="sxs-lookup"><span data-stu-id="c875c-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="c875c-109">Se você definir *enumTocPosType* como **índice \_ de \_ PDV de Sumário**, o método retornará **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="c875c-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="c875c-110">Os métodos a seguir têm um parâmetro *enumTocPosType* .</span><span class="sxs-lookup"><span data-stu-id="c875c-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="c875c-111">**GetTocCount**</span><span class="sxs-lookup"><span data-stu-id="c875c-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="c875c-112">**GetTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="c875c-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="c875c-113">**GetTocByType**</span><span class="sxs-lookup"><span data-stu-id="c875c-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="c875c-114">**AddToc**</span><span class="sxs-lookup"><span data-stu-id="c875c-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="c875c-115">**RemoveTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="c875c-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="c875c-116">**RemoveTocByType**</span><span class="sxs-lookup"><span data-stu-id="c875c-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="c875c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c875c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c875c-118">Guia de programação do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="c875c-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



