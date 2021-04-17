---
description: Como criar uma DLL de filtro do DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Como criar uma DLL de filtro do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747801"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="5a8b4-103">Como criar uma DLL de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5a8b4-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="5a8b4-104">Este artigo descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5a8b4-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="5a8b4-105">Este artigo é uma continuação de [como implementar IUnknown](how-to-implement-iunknown.md), que descreve como implementar a interface **IUnknown** derivando seu componente da classe base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8b4-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="5a8b4-106">Este artigo inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a8b4-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="5a8b4-107">Fábricas de classes e modelos de fábrica</span><span class="sxs-lookup"><span data-stu-id="5a8b4-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="5a8b4-108">Matriz de modelo de fábrica</span><span class="sxs-lookup"><span data-stu-id="5a8b4-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="5a8b4-109">Funções de DLL</span><span class="sxs-lookup"><span data-stu-id="5a8b4-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="5a8b4-110">O registro de um filtro do DirectShow (em oposição a um objeto COM genérico) requer algumas etapas adicionais que não são abordadas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="5a8b4-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="5a8b4-111">Para obter informações sobre como registrar filtros, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5a8b4-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a8b4-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a8b4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8b4-113">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="5a8b4-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



