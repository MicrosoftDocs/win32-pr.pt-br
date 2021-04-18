---
description: Etapa 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Etapa 9. Desconectar a página de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810382"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="b4f1e-104">Etapa 9.</span><span class="sxs-lookup"><span data-stu-id="b4f1e-104">Step 9.</span></span> <span data-ttu-id="b4f1e-105">Desconectar a página de propriedades</span><span class="sxs-lookup"><span data-stu-id="b4f1e-105">Disconnect the Property Page</span></span>

<span data-ttu-id="b4f1e-106">Substitua o método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) para liberar as interfaces que você obteve no método **OnConnect** .</span><span class="sxs-lookup"><span data-stu-id="b4f1e-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="b4f1e-107">Além disso, se o usuário ignorar a folha de propriedades sem confirmar as alterações, você deverá restaurar os valores originais se eles tiverem mudado.</span><span class="sxs-lookup"><span data-stu-id="b4f1e-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="b4f1e-108">Não há nenhum método "OnCancel" que é chamado quando o usuário cancela, portanto, você precisa controlar se o usuário chamou **OnApplyChanges**.</span><span class="sxs-lookup"><span data-stu-id="b4f1e-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="b4f1e-109">Este exemplo usa a \_ variável m LVAL, descrita anteriormente:</span><span class="sxs-lookup"><span data-stu-id="b4f1e-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="b4f1e-110">Em seguida: [etapa 10. Suporte ao registro COM](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="b4f1e-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4f1e-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4f1e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4f1e-112">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="b4f1e-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



