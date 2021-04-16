---
description: Etapa 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Etapa 8. Aplicar alterações de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758507"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="d0638-104">Etapa 8.</span><span class="sxs-lookup"><span data-stu-id="d0638-104">Step 8.</span></span> <span data-ttu-id="d0638-105">Aplicar alterações de propriedade</span><span class="sxs-lookup"><span data-stu-id="d0638-105">Apply Property Changes</span></span>

<span data-ttu-id="d0638-106">Substitua o método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) para confirmar qualquer alteração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0638-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="d0638-107">Neste exemplo, a variável m \_ lNewVal é atualizada sempre que o usuário rola a barra deslizante.</span><span class="sxs-lookup"><span data-stu-id="d0638-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="d0638-108">O método **OnApplyChanges** copia esse valor na variável m \_ LVAL, substituindo o valor original:</span><span class="sxs-lookup"><span data-stu-id="d0638-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="d0638-109">Em seguida: [etapa 9. Desconecte a página de propriedades](step-9--disconnect-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="d0638-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0638-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0638-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0638-111">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="d0638-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



