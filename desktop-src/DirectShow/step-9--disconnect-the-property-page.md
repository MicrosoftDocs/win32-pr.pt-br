---
description: Etapa 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Etapa 9. Desconectar a página de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526076"
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

 

 



