---
title: Estruturas-StoServe
description: O copaper empacota a cor, a largura e as coordenadas da caneta em estruturas INKDATA e as armazena em uma matriz alocada dinamicamente que ela gerencia na memória.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916172"
---
# <a name="structures---stoserve"></a><span data-ttu-id="b78fb-103">Estruturas-StoServe</span><span class="sxs-lookup"><span data-stu-id="b78fb-103">Structures - StoServe</span></span>

<span data-ttu-id="b78fb-104">O copaper empacota a cor, a largura e as coordenadas da caneta em estruturas **INKDATA** e as armazena em uma matriz alocada dinamicamente que ela gerencia na memória.</span><span class="sxs-lookup"><span data-stu-id="b78fb-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="b78fb-105">Estrutura INKDATA</span><span class="sxs-lookup"><span data-stu-id="b78fb-105">INKDATA Structure</span></span>

<span data-ttu-id="b78fb-106">A seguir estão as declarações para a estrutura **INKDATA** do paper. H.</span><span class="sxs-lookup"><span data-stu-id="b78fb-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

<span data-ttu-id="b78fb-107">A matriz dinâmica desses pacotes **INKDATA** é apontada por m \_ paInkData, um membro da classe de implementação [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="b78fb-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="b78fb-108">A matriz é criada dentro do método **IPaper:: InitPaper** com uma alocação inicial.</span><span class="sxs-lookup"><span data-stu-id="b78fb-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="b78fb-109">Para obter detalhes, consulte o método **InitPaper** e o método de utilitário NextSlot privado da implementação CIMPIPAPER em Paper. H.</span><span class="sxs-lookup"><span data-stu-id="b78fb-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="b78fb-110">Os métodos [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usam NextSlot para obter novos slots na matriz.</span><span class="sxs-lookup"><span data-stu-id="b78fb-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="b78fb-111">A matriz é expandida dinamicamente pelo NextSlot à medida que surge a necessidade.</span><span class="sxs-lookup"><span data-stu-id="b78fb-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="b78fb-112">O cliente chama o método [**IPaper:: Erase**](ipaper-methods.md) para apagar o desenho atual.</span><span class="sxs-lookup"><span data-stu-id="b78fb-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="b78fb-113">Esse método não realoca a matriz; Ele simplesmente marca todos os dados de tinta atuais como INKTYPE \_ None e redefine o índice de fim de dados da matriz como zero.</span><span class="sxs-lookup"><span data-stu-id="b78fb-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="b78fb-114">O cliente chama os métodos [**IPaper:: Lock**](ipaper-methods.md) e **Unlock** para gerenciar a propriedade de copapel para desenho.</span><span class="sxs-lookup"><span data-stu-id="b78fb-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="b78fb-115">Esses métodos são fornecidos para organizar o acesso entre vários clientes no desenho mantido em um copapel compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b78fb-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="b78fb-116">Estrutura de propriedades do papel \_</span><span class="sxs-lookup"><span data-stu-id="b78fb-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="b78fb-117">O cliente chama o método [**IPaper:: Resize**](ipaper-methods.md) para informar ao copaper que o usuário redimensionou o retângulo do papel de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="b78fb-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="b78fb-118">Esses dados de coordenadas são mantidos em uma estrutura de **\_ Propriedades de papel** , que é armazenada com os dados de tinta quando todos os dados de papel são armazenados em um arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="b78fb-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="b78fb-119">A seguir está a declaração de **\_ Propriedades de papel** do paper. H.</span><span class="sxs-lookup"><span data-stu-id="b78fb-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

<span data-ttu-id="b78fb-120">A estrutura de **\_ Propriedades de papel** foi projetada para que novos formatos de dados de tinta possam ser adicionados a qualquer momento, à medida que o componente DllPaper evoluir.</span><span class="sxs-lookup"><span data-stu-id="b78fb-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="b78fb-121">A interface [**IPaper**](ipaper-methods.md) é geral o suficiente para que uma versão subsequente do componente DllPaper possa armazenar um formato de dados de tinta diferente ao implementar a mesma interface **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="b78fb-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="b78fb-122">Como os métodos de **IPaper** não dependem de um formato de dados de tinta específico, uma nova versão do componente DllPaper que dá suporte a um formato de dados de tinta diferente pode usar essa mesma interface.</span><span class="sxs-lookup"><span data-stu-id="b78fb-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="b78fb-123">As propriedades de papel armazenadas em um arquivo composto registram o tamanho atual da matriz de dados de tinta.</span><span class="sxs-lookup"><span data-stu-id="b78fb-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="b78fb-124">O tamanho de matriz adequado pode ser alocado para acomodar os dados de tinta lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b78fb-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="b78fb-125">A estrutura de **\_ Propriedades de papel** também armazena a cor da janela de plano de fundo e o tamanho do retângulo de desenho da superfície de papel.</span><span class="sxs-lookup"><span data-stu-id="b78fb-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="b78fb-126">Embora não seja usado nos exemplos de **StoServe** / **StoClien** , um título de desenho e um nome de autor também podem ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="b78fb-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="b78fb-127">A data de criação e as datas da última modificação não são incluídas nessas propriedades de papel, pois a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usada para acessar arquivos compostos gerencia essas informações.</span><span class="sxs-lookup"><span data-stu-id="b78fb-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 




