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
# <a name="step-5-store-a-pointer-to-the-filter"></a>Etapa 5. Armazenar um ponteiro para o filtro

Substitua o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) para armazenar um ponteiro para o filtro. O exemplo a seguir consulta o parâmetro *punk* para a interface ISaturation personalizada do filtro:


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



Em seguida: [etapa 6. Inicialize a caixa de diálogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



