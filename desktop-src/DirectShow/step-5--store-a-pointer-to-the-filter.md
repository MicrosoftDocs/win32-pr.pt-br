---
description: Etapa 5.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Etapa 5. Armazenar um ponteiro para o filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff096c6afcf830494ef02920176d8f80a3b9569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170969"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="2947f-104">Etapa 5.</span><span class="sxs-lookup"><span data-stu-id="2947f-104">Step 5.</span></span> <span data-ttu-id="2947f-105">Armazenar um ponteiro para o filtro</span><span class="sxs-lookup"><span data-stu-id="2947f-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="2947f-106">Substitua o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) para armazenar um ponteiro para o filtro.</span><span class="sxs-lookup"><span data-stu-id="2947f-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="2947f-107">O exemplo a seguir consulta o parâmetro *punk* para a interface ISaturation personalizada do filtro:</span><span class="sxs-lookup"><span data-stu-id="2947f-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="2947f-108">Em seguida: [etapa 6. Inicialize a caixa de diálogo](step-6--initialize-the-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="2947f-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2947f-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2947f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2947f-110">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="2947f-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



