---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170662"
---
# <a name="blob-components"></a><span data-ttu-id="6845b-103">Componentes de BLOB</span><span class="sxs-lookup"><span data-stu-id="6845b-103">BLOB Components</span></span>

<span data-ttu-id="6845b-104">Um BLOB (objeto binário grande) inclui os seguintes componentes hierárquicos:</span><span class="sxs-lookup"><span data-stu-id="6845b-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="6845b-105">Proprietários</span><span class="sxs-lookup"><span data-stu-id="6845b-105">Owners</span></span>
-   <span data-ttu-id="6845b-106">Categorias</span><span class="sxs-lookup"><span data-stu-id="6845b-106">Categories</span></span>
-   <span data-ttu-id="6845b-107">Marcações</span><span class="sxs-lookup"><span data-stu-id="6845b-107">Tags</span></span>
-   <span data-ttu-id="6845b-108">Valores</span><span class="sxs-lookup"><span data-stu-id="6845b-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="6845b-109">Representação textual</span><span class="sxs-lookup"><span data-stu-id="6845b-109">Textual Representation</span></span>

<span data-ttu-id="6845b-110">Para sua conveniência, os BLOBs aparecem no formato proprietário: Categoria: marca: valor que eles aparecem quando salvos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6845b-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="6845b-111">A estrutura interna do BLOB é opaca porque ele representa ponteiros e tabelas.</span><span class="sxs-lookup"><span data-stu-id="6845b-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="6845b-112">Por exemplo, aqui está uma entrada de um BLOB que pode ser usada para configurar um NPP:</span><span class="sxs-lookup"><span data-stu-id="6845b-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="6845b-113">O proprietário é NPP.</span><span class="sxs-lookup"><span data-stu-id="6845b-113">The Owner is NPP.</span></span> <span data-ttu-id="6845b-114">A categoria é configurada, a marca é BufferSize e o valor é 32768.</span><span class="sxs-lookup"><span data-stu-id="6845b-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



