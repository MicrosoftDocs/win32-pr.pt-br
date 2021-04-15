---
title: Classes, objetos e interfaces
description: Classes, objetos e interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104454445"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="f6b02-103">Classes, objetos e interfaces</span><span class="sxs-lookup"><span data-stu-id="f6b02-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="f6b02-104">Na linguagem de programação C++, uma *classe* consiste em *Propriedades* (ou dados de membros) e *métodos* (ou funções de membro).</span><span class="sxs-lookup"><span data-stu-id="f6b02-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="f6b02-105">As propriedades são elementos de dados, como os contidos em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="f6b02-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="f6b02-106">Os métodos são usados para uma variedade de finalidades, como inicialização, atribuição, operações e acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="f6b02-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="f6b02-107">Você usa uma declaração de classe da mesma maneira que usa uma declaração de estrutura.</span><span class="sxs-lookup"><span data-stu-id="f6b02-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="f6b02-108">A memória é alocada para uma classe quando você define um *objeto* de classe.</span><span class="sxs-lookup"><span data-stu-id="f6b02-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="f6b02-109">Cada objeto de classe tem uma área de dados para suas propriedades e uma tabela de ponteiros para os métodos aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="f6b02-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="f6b02-110">No OLE, um objeto consiste em dados e métodos, como acontece em C++.</span><span class="sxs-lookup"><span data-stu-id="f6b02-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="f6b02-111">No entanto, um objeto OLE segue regras mais rígidas.</span><span class="sxs-lookup"><span data-stu-id="f6b02-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="f6b02-112">Os dados são estritamente internos.</span><span class="sxs-lookup"><span data-stu-id="f6b02-112">The data is strictly internal.</span></span> <span data-ttu-id="f6b02-113">Um objeto expõe apenas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f6b02-113">An object only exposes interfaces.</span></span> <span data-ttu-id="f6b02-114">Uma *interface* é um conjunto de métodos relacionados para um objeto.</span><span class="sxs-lookup"><span data-stu-id="f6b02-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="f6b02-115">Cada objeto pode dar suporte a várias interfaces.</span><span class="sxs-lookup"><span data-stu-id="f6b02-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="f6b02-116">Todas as interfaces OLE dão suporte à interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f6b02-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




