---
title: O que um cliente vê
description: Este tópico lista maneiras que um cliente exibe dados ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, o que um cliente vê
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499151"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="131af-104">O que um cliente vê?</span><span class="sxs-lookup"><span data-stu-id="131af-104">What Does a Client See?</span></span>

-   <span data-ttu-id="131af-105">Um cliente vê ADSI e todos os seus objetos de extensão como um objeto.</span><span class="sxs-lookup"><span data-stu-id="131af-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="131af-106">Um cliente ADSI vê uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que manipula todas as interfaces duplas e de expedição no objeto, se a interface de expedição ou dupla é implementada pelo agregador no provedor ou por uma extensão.</span><span class="sxs-lookup"><span data-stu-id="131af-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="131af-107">Consulte a [resolução de conflitos de nome de função/Propriedade em automação em extensões](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="131af-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="131af-108">A ADSI não expõe nenhuma informação de tipo pelos métodos [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ou [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) .</span><span class="sxs-lookup"><span data-stu-id="131af-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="131af-109">A ADSI fornece informações de tipo por meio da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="131af-109">ADSI provides type information through the type library.</span></span>

 

 