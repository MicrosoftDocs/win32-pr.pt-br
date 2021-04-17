---
title: Verificando valores de retorno do IAccessible
description: Os desenvolvedores de cliente não devem confiar nas macros de Component Object Model (COM) com êxito e FALHAram em testar os valores de retorno de IAccessible, pois valores diferentes de S \_ OK são considerados um sucesso.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812059"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="cc64a-103">Verificando valores de retorno do IAccessible</span><span class="sxs-lookup"><span data-stu-id="cc64a-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="cc64a-104">Os desenvolvedores de cliente não devem confiar nas macros de Component Object Model (COM) com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**falharam**](/windows/desktop/api/winerror/nf-winerror-failed) em testar os valores de retorno de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , pois valores diferentes de S \_ OK são considerados um sucesso.</span><span class="sxs-lookup"><span data-stu-id="cc64a-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="cc64a-105">Por exemplo, um método pode retornar S \_ false, que é considerado um sucesso pela macro **Succeeded** , mas ainda recebe um ponteiro **NULL** em um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="cc64a-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="cc64a-106">Os desenvolvedores de cliente devem se proteger contra a possibilidade de que alguns servidores retornem códigos de erro diferentes dos valores documentados.</span><span class="sxs-lookup"><span data-stu-id="cc64a-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="cc64a-107">Para ser seguro, você deve garantir que todos os parâmetros de saída contenham informações válidas e atendam aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="cc64a-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="cc64a-108">Todos os ponteiros são não **nulos**.</span><span class="sxs-lookup"><span data-stu-id="cc64a-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="cc64a-109">O membro **VT** de qualquer estrutura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) não é igual a VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="cc64a-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 