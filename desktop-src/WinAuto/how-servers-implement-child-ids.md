---
title: Como os servidores implementam IDs filho
description: Os desenvolvedores de servidor podem atribuir IDs filho a elementos simples e objetos acessíveis. No entanto, a abordagem recomendada é oferecer suporte à interface de Component Object Model padrão (COM) IEnumVARIANT em todos os objetos acessíveis que tenham filhos.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917476"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="64f96-104">Como os servidores implementam IDs filho</span><span class="sxs-lookup"><span data-stu-id="64f96-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="64f96-105">Os desenvolvedores de servidor podem atribuir IDs filho a elementos simples e objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="64f96-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="64f96-106">No entanto, a abordagem recomendada é oferecer suporte à interface de Component Object Model padrão (COM) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em todos os objetos acessíveis que tenham filhos.</span><span class="sxs-lookup"><span data-stu-id="64f96-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="64f96-107">Se você implementar o [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), deverá:</span><span class="sxs-lookup"><span data-stu-id="64f96-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="64f96-108">Enumere todos os filhos, tanto elementos simples quanto objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="64f96-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="64f96-109">Forneça IDs filho para todos os elementos simples e forneça o [**IDispatch**](idispatch-interface.md) para cada objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="64f96-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="64f96-110">Para objetos acessíveis, defina o membro **VT** da expedição de [**variante**](variant-structure.md) para VT \_ .</span><span class="sxs-lookup"><span data-stu-id="64f96-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="64f96-111">O membro **pdispVal** deve conter um ponteiro para a interface [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="64f96-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="64f96-112">Observe que a **variante** é alocada e liberada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="64f96-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="64f96-113">Para elementos simples, a ID filho é qualquer número inteiro positivo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64f96-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="64f96-114">Observe que os inteiros zero e negativos são reservados pelo Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="64f96-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="64f96-115">Defina o membro **VT** da estrutura [**variante**](variant-structure.md) como VT \_ i4 e o membro **lVal** como a ID filho.</span><span class="sxs-lookup"><span data-stu-id="64f96-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="64f96-116">Se você não oferecer suporte a [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), deverá atribuir IDs filho e numerar os filhos em cada objeto de forma sequencial, começando com um.</span><span class="sxs-lookup"><span data-stu-id="64f96-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="64f96-117">É recomendável que os clientes usem a função Microsoft Acessibilidade Ativa [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) em vez de chamar a interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) do servidor diretamente.</span><span class="sxs-lookup"><span data-stu-id="64f96-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 