---
title: Diretrizes de COM e Unicode
description: Como o Microsoft Acessibilidade Ativa se baseia em Component Object Model (COM), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772610"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="1c90c-103">Diretrizes de COM e Unicode</span><span class="sxs-lookup"><span data-stu-id="1c90c-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="1c90c-104">Como o Microsoft Acessibilidade Ativa se baseia em Component Object Model (COM), os desenvolvedores precisam de um nível moderado de compreensão sobre objetos e interfaces COM e devem saber como executar tarefas básicas (por exemplo, como inicializar a biblioteca COM).</span><span class="sxs-lookup"><span data-stu-id="1c90c-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="1c90c-105">Os desenvolvedores de servidor precisam entender como projetar classes que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e como criar objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="1c90c-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="1c90c-106">Você também precisa de um nível moderado de compreensão sobre o Unicode para usar muitas das funções do Microsoft Acessibilidade Ativa que retornam cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1c90c-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="1c90c-107">Para usar o Microsoft Acessibilidade Ativa com eficiência, você deve entender as seguintes funções e estruturas de COM e Unicode, estrutura, tipos de dados e interfaces.</span><span class="sxs-lookup"><span data-stu-id="1c90c-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="1c90c-108">Informações limitadas sobre alguns desses itens são fornecidas nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="1c90c-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="1c90c-109">Funções:</span><span class="sxs-lookup"><span data-stu-id="1c90c-109">Functions:</span></span>

-   [<span data-ttu-id="1c90c-110">**OleInitialize**</span><span class="sxs-lookup"><span data-stu-id="1c90c-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="1c90c-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="1c90c-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="1c90c-112">[**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="1c90c-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="1c90c-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) e [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="1c90c-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="1c90c-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="1c90c-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="1c90c-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="1c90c-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="1c90c-116">Estruturas e tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="1c90c-116">Structures and data types:</span></span>

-   [<span data-ttu-id="1c90c-117">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="1c90c-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="1c90c-118">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1c90c-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="1c90c-119">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="1c90c-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="1c90c-120">Interfaces COM:</span><span class="sxs-lookup"><span data-stu-id="1c90c-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="1c90c-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="1c90c-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="1c90c-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1c90c-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="1c90c-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="1c90c-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="1c90c-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1c90c-124">In this section</span></span>

-   [<span data-ttu-id="1c90c-125">Estrutura de variante</span><span class="sxs-lookup"><span data-stu-id="1c90c-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="1c90c-126">Interface IDispatch</span><span class="sxs-lookup"><span data-stu-id="1c90c-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="1c90c-127">Convertendo cadeias de caracteres Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1c90c-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 