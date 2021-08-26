---
description: Armazene um ponteiro para um filtro como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: Etapa 5. Armazenar um ponteiro para o filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078766"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>Etapa 5. Armazenar um ponteiro para o filtro

Substitua o [**método CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) para armazenar um ponteiro para o filtro. O exemplo a seguir consulta o *parâmetro pUnk* para a interface de IS saturação personalizada do filtro:


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



Próximo: [Etapa 6. Inicialize a caixa de diálogo](step-6--initialize-the-dialog.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



