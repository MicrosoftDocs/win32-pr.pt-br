---
title: O cabeçalho ACF
description: O cabeçalho ACF contém atributos específicos da plataforma que se aplicam à interface como um todo. Os atributos aplicados a tipos individuais e funções no corpo de ACF substituem os atributos no cabeçalho ACF. Nenhum atributo é necessário no cabeçalho ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007827"
---
# <a name="the-acf-header"></a><span data-ttu-id="59eca-105">O cabeçalho ACF</span><span class="sxs-lookup"><span data-stu-id="59eca-105">The ACF Header</span></span>

<span data-ttu-id="59eca-106">O cabeçalho ACF contém atributos específicos da plataforma que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="59eca-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="59eca-107">Os atributos aplicados a tipos individuais e funções no corpo de ACF substituem os atributos no cabeçalho ACF.</span><span class="sxs-lookup"><span data-stu-id="59eca-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="59eca-108">Nenhum atributo é necessário no cabeçalho ACF.</span><span class="sxs-lookup"><span data-stu-id="59eca-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="59eca-109">O cabeçalho ACF pode incluir um dos seguintes atributos: **\[** [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** ou [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="59eca-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="59eca-110">Se o **\[ \_ identificador \] automático** ou o **\[ \_ \] identificador implícito** for usado, ele especificará o tipo de identificador de associação que será usado para associação quando uma função remota não tiver um parâmetro de identificador de ligação explícito.</span><span class="sxs-lookup"><span data-stu-id="59eca-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="59eca-111">Quando o ACF não está presente ou não especifica um identificador de associação automático, implícito ou explícito, MIDL usa o **\[ \_ identificador \] auto** para associação implícita.</span><span class="sxs-lookup"><span data-stu-id="59eca-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="59eca-112">O **\[** [**código**](/windows/desktop/Midl/code) **\]** ou o **\[** [**Nocode**](/windows/desktop/Midl/nocode) **\]** podem aparecer no cabeçalho da interface, mas o que você escolher pode aparecer apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="59eca-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="59eca-113">Quando nenhum atributo estiver presente, o compilador usará o **\[ código \]** como padrão.</span><span class="sxs-lookup"><span data-stu-id="59eca-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="59eca-114">Para obter mais informações, consulte [atributos de ACF](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="59eca-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 