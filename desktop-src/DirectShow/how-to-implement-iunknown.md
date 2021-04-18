---
description: Como implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Como implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500162"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="b90c8-103">Como implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="b90c8-103">How to Implement IUnknown</span></span>

<span data-ttu-id="b90c8-104">O Microsoft DirectShow é baseado na Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="b90c8-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="b90c8-105">Se você escrever seu próprio filtro, deverá implementá-lo como um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="b90c8-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="b90c8-106">As classes base do DirectShow fornecem uma estrutura da qual fazer isso.</span><span class="sxs-lookup"><span data-stu-id="b90c8-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="b90c8-107">Não é necessário usar as classes base, mas isso pode simplificar o processo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b90c8-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="b90c8-108">Este artigo descreve alguns dos detalhes internos de objetos COM e sua implementação nas classes base do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b90c8-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="b90c8-109">Este artigo pressupõe que você saiba como programar aplicativos cliente COM, em outras palavras, que você entende os métodos em **IUnknown**, mas não assume nenhuma experiência anterior ao desenvolver objetos com.</span><span class="sxs-lookup"><span data-stu-id="b90c8-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="b90c8-110">O DirectShow lida com muitos dos detalhes do desenvolvimento de um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="b90c8-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="b90c8-111">Se tiver experiência em desenvolver objetos COM, você deverá ler a seção [usando CUnknown](using-cunknown.md), que descreve a classe base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b90c8-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="b90c8-112">COM é uma especificação, não uma implementação.</span><span class="sxs-lookup"><span data-stu-id="b90c8-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="b90c8-113">Ele define as regras que um componente deve seguir; colocar essas regras em vigor é deixado para o desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="b90c8-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="b90c8-114">No DirectShow, todos os objetos derivam de um conjunto de classes base C++.</span><span class="sxs-lookup"><span data-stu-id="b90c8-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="b90c8-115">Os construtores e métodos de classe base fazem a maior parte do trabalho de "escrituração" COM, como manter uma contagem de referência consistente.</span><span class="sxs-lookup"><span data-stu-id="b90c8-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="b90c8-116">Ao derivar o filtro de uma classe base, você herda a funcionalidade da classe.</span><span class="sxs-lookup"><span data-stu-id="b90c8-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="b90c8-117">Para usar classes base COM eficiência, você precisa de uma compreensão geral de como elas implementam a especificação COM.</span><span class="sxs-lookup"><span data-stu-id="b90c8-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="b90c8-118">Este artigo contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b90c8-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="b90c8-119">Como o IUnknown funciona</span><span class="sxs-lookup"><span data-stu-id="b90c8-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="b90c8-120">Usando CUnknown</span><span class="sxs-lookup"><span data-stu-id="b90c8-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="b90c8-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b90c8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b90c8-122">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="b90c8-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



