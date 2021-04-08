---
title: Controles de edição avançados sem janela
description: Esta seção contém informações sobre os elementos de programação usados com controles de edição ricos sem janela.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005122"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="f55d5-103">Controles de edição avançados sem janela</span><span class="sxs-lookup"><span data-stu-id="f55d5-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="f55d5-104">Esta seção contém informações sobre os elementos de programação usados com controles de edição ricos sem janela.</span><span class="sxs-lookup"><span data-stu-id="f55d5-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="f55d5-105">O COM (Component Object Model) define um conjunto de interfaces para oferecer suporte a objetos sem janela.</span><span class="sxs-lookup"><span data-stu-id="f55d5-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="f55d5-106">Os objetos sem janela podem entrar no estado ativo no local não ter sua própria janela, mas sim usar a janela de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="f55d5-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="f55d5-107">Consequentemente, um objeto sem janela usa menos recursos do sistema e oferece melhor desempenho por meio de ativação e desativação mais rápida.</span><span class="sxs-lookup"><span data-stu-id="f55d5-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="f55d5-108">Além disso, os objetos sem janela podem ser não retangulares e transparentes.</span><span class="sxs-lookup"><span data-stu-id="f55d5-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="f55d5-109">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="f55d5-109">Overviews</span></span>



| <span data-ttu-id="f55d5-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="f55d5-110">Topic</span></span>                                                                          | <span data-ttu-id="f55d5-111">Sumário</span><span class="sxs-lookup"><span data-stu-id="f55d5-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f55d5-112">Sobre controles de edição avançados sem janela</span><span class="sxs-lookup"><span data-stu-id="f55d5-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="f55d5-113">Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um [controle de edição rico](rich-edit-controls.md) sem fornecer a janela.</span><span class="sxs-lookup"><span data-stu-id="f55d5-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="f55d5-114">Funções</span><span class="sxs-lookup"><span data-stu-id="f55d5-114">Functions</span></span>



| <span data-ttu-id="f55d5-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="f55d5-115">Topic</span></span>                                            | <span data-ttu-id="f55d5-116">Sumário</span><span class="sxs-lookup"><span data-stu-id="f55d5-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f55d5-117">**Createtextservices**</span><span class="sxs-lookup"><span data-stu-id="f55d5-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="f55d5-118">A função [**Createtextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) cria uma instância de um objeto de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="f55d5-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="f55d5-119">O objeto de serviços de texto dá suporte a uma variedade de interfaces, incluindo [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e o Tom (modelo de objeto de texto).</span><span class="sxs-lookup"><span data-stu-id="f55d5-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="f55d5-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f55d5-120">Interfaces</span></span>



| <span data-ttu-id="f55d5-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="f55d5-121">Topic</span></span>                                  | <span data-ttu-id="f55d5-122">Sumário</span><span class="sxs-lookup"><span data-stu-id="f55d5-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f55d5-123">**ITextHost**</span><span class="sxs-lookup"><span data-stu-id="f55d5-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="f55d5-124">A interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) é usada por um objeto de serviços de texto para obter os serviços de host de texto.</span><span class="sxs-lookup"><span data-stu-id="f55d5-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="f55d5-125">**ITextServices**</span><span class="sxs-lookup"><span data-stu-id="f55d5-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="f55d5-126">Estende o TOM para fornecer funcionalidade extra para operação sem janelas.</span><span class="sxs-lookup"><span data-stu-id="f55d5-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





