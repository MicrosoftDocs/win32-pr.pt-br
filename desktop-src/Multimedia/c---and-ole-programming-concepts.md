---
title: Conceitos de programação C++ e OLE
description: Conceitos de programação C++ e OLE
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823032"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="4af3c-103">Conceitos de programação C++ e OLE</span><span class="sxs-lookup"><span data-stu-id="4af3c-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="4af3c-104">Os manipuladores de arquivo e fluxo incluídos no Windows usam um design orientado a objeto para promover uma interface padrão e compartilhar a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="4af3c-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="4af3c-105">Esses manipuladores são escritos em C++ e usam o Component Object Model OLE.</span><span class="sxs-lookup"><span data-stu-id="4af3c-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="4af3c-106">Você pode desenvolver manipuladores personalizados usando os sistemas de desenvolvimento C ou C++; no entanto, o uso do C++ é altamente recomendável, pois fornece uma abordagem mais fácil e direta para implementar um manipulador.</span><span class="sxs-lookup"><span data-stu-id="4af3c-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="4af3c-107">Usando C++, você pode definir explicitamente dados como objetos e associar as funções que manipulam os dados com as funções de membro de um objeto.</span><span class="sxs-lookup"><span data-stu-id="4af3c-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="4af3c-108">Esta seção identifica e resume brevemente os conceitos importantes do C++ e do Component Object Model OLE que se aplicam ao design e à implementação de manipuladores de arquivo e de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4af3c-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="4af3c-109">Há muitos livros escritos sobre a programação em C++ que você pode referenciar para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4af3c-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="4af3c-110">Para obter mais informações sobre OLE, consulte a *referência do programador de OLE*.</span><span class="sxs-lookup"><span data-stu-id="4af3c-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




