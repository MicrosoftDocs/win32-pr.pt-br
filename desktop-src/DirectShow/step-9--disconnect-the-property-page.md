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
# <a name="step-9-disconnect-the-property-page"></a>Etapa 9. Desconectar a página de propriedades

Substitua o método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) para liberar as interfaces que você obteve no método **OnConnect** . Além disso, se o usuário ignorar a folha de propriedades sem confirmar as alterações, você deverá restaurar os valores originais se eles tiverem mudado. Não há nenhum método "OnCancel" que é chamado quando o usuário cancela, portanto, você precisa controlar se o usuário chamou **OnApplyChanges**. Este exemplo usa a \_ variável m LVAL, descrita anteriormente:


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



Em seguida: [etapa 10. Suporte ao registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



