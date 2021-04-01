---
title: Estrutura de variante
description: A maioria das funções do Microsoft Acessibilidade Ativa e os métodos e as propriedades do IAccessible usam uma estrutura variante como parâmetro. Essencialmente, a estrutura variante é um contêiner para uma União grande que transporta muitos tipos de dados.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084658"
---
# <a name="variant-structure"></a><span data-ttu-id="36e3d-104">Estrutura de variante</span><span class="sxs-lookup"><span data-stu-id="36e3d-104">VARIANT Structure</span></span>

<span data-ttu-id="36e3d-105">A maioria das funções do Microsoft Acessibilidade Ativa e os métodos e as propriedades do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) usam uma estrutura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="36e3d-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="36e3d-106">Essencialmente, a estrutura **variante** é um contêiner para uma União grande que transporta muitos tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="36e3d-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="36e3d-107">O valor no primeiro membro da estrutura, **VT**, descreve qual dos membros da União é válido.</span><span class="sxs-lookup"><span data-stu-id="36e3d-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="36e3d-108">Embora a estrutura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) ofereça suporte a muitos tipos de dados diferentes, o Microsoft Acessibilidade Ativa usa apenas os tipos a seguir.</span><span class="sxs-lookup"><span data-stu-id="36e3d-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="36e3d-109">Valor de VT</span><span class="sxs-lookup"><span data-stu-id="36e3d-109">vt Value</span></span>     | <span data-ttu-id="36e3d-110">Nome do membro do valor correspondente</span><span class="sxs-lookup"><span data-stu-id="36e3d-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="36e3d-111">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="36e3d-111">VT\_I4</span></span>       | <span data-ttu-id="36e3d-112">**lVal**</span><span class="sxs-lookup"><span data-stu-id="36e3d-112">**lVal**</span></span>                        |
| <span data-ttu-id="36e3d-113">expedição de VT \_</span><span class="sxs-lookup"><span data-stu-id="36e3d-113">VT\_DISPATCH</span></span> | <span data-ttu-id="36e3d-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="36e3d-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="36e3d-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="36e3d-115">VT\_BSTR</span></span>     | <span data-ttu-id="36e3d-116">**bstrVal**</span><span class="sxs-lookup"><span data-stu-id="36e3d-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="36e3d-117">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="36e3d-117">VT\_EMPTY</span></span>    | <span data-ttu-id="36e3d-118">none</span><span class="sxs-lookup"><span data-stu-id="36e3d-118">none</span></span>                            |



 

<span data-ttu-id="36e3d-119">Ao receber informações em uma estrutura de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , verifique o membro **VT** para descobrir qual membro contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="36e3d-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="36e3d-120">Da mesma forma, quando você envia informações usando uma estrutura **Variant** , sempre defina **VT** para refletir o membro Union que contém as informações.</span><span class="sxs-lookup"><span data-stu-id="36e3d-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="36e3d-121">Antes de usar a estrutura, inicialize-a chamando a função COM ( [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="36e3d-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="36e3d-122">Quando terminar com a estrutura, limpe-a antes que a memória que contém a [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) seja liberada chamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span><span class="sxs-lookup"><span data-stu-id="36e3d-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 