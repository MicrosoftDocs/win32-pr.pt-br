---
description: Armazene um ponteiro para um filtro como parte da criação de uma página de propriedades de filtro para um filtro do DirectShow personalizado.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Etapa 5. Armazenar um ponteiro para o filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406789"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="dd463-104">Etapa 5.</span><span class="sxs-lookup"><span data-stu-id="dd463-104">Step 5.</span></span> <span data-ttu-id="dd463-105">Armazenar um ponteiro para o filtro</span><span class="sxs-lookup"><span data-stu-id="dd463-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="dd463-106">Substitua o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) para armazenar um ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="dd463-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="dd463-107">O exemplo a seguir consulta o parâmetro *punk* para a interface ISaturation personalizada do filtro:</span><span class="sxs-lookup"><span data-stu-id="dd463-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



<span data-ttu-id="dd463-108">Em seguida: [etapa 6. Inicialize a caixa de diálogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="dd463-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd463-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd463-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd463-110">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="dd463-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



