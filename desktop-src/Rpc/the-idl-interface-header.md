---
title: O cabeçalho da interface IDL
description: O cabeçalho da interface IDL especifica informações sobre a interface como um todo. Ao contrário do ACF, o cabeçalho da interface contém atributos que são independentes de plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084864"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="d0a42-104">O cabeçalho da interface IDL</span><span class="sxs-lookup"><span data-stu-id="d0a42-104">The IDL Interface Header</span></span>

<span data-ttu-id="d0a42-105">O cabeçalho da interface IDL especifica informações sobre a interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="d0a42-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="d0a42-106">Ao contrário do ACF, o cabeçalho da interface contém atributos que são independentes de plataforma.</span><span class="sxs-lookup"><span data-stu-id="d0a42-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="d0a42-107">Os atributos no cabeçalho da interface são globais para toda a interface.</span><span class="sxs-lookup"><span data-stu-id="d0a42-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="d0a42-108">Ou seja, eles se aplicam à interface e a todas as suas partes.</span><span class="sxs-lookup"><span data-stu-id="d0a42-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="d0a42-109">Esses atributos são colocados entre colchetes no início da definição da interface.</span><span class="sxs-lookup"><span data-stu-id="d0a42-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="d0a42-110">Um exemplo é mostrado na seguinte definição de interface:</span><span class="sxs-lookup"><span data-stu-id="d0a42-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="d0a42-111">Observe que o cabeçalho da interface contém os **\[** atributos [**UUID**](/windows/desktop/Midl/uuid) **\]** e **\[** [**version**](/windows/desktop/Midl/version) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d0a42-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="d0a42-112">Como eles representam o UUID e o número de versão da interface, respectivamente, eles são atributos de toda a interface.</span><span class="sxs-lookup"><span data-stu-id="d0a42-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="d0a42-113">O corpo da interface também pode conter atributos.</span><span class="sxs-lookup"><span data-stu-id="d0a42-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="d0a42-114">No entanto, eles não são aplicáveis à interface inteira.</span><span class="sxs-lookup"><span data-stu-id="d0a42-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="d0a42-115">Eles se referem a itens específicos na interface, como parâmetros de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="d0a42-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="d0a42-116">Para obter uma discussão completa sobre os atributos de cabeçalho IDL, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="d0a42-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 