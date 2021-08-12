---
description: Etapa 8.
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: Etapa 8. Aplicar alterações de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652052"
---
# <a name="step-8-apply-property-changes"></a>Etapa 8. Aplicar alterações de propriedade

Substitua o método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) para confirmar qualquer alteração de propriedade. Neste exemplo, a variável m \_ lNewVal é atualizada sempre que o usuário rola a barra deslizante. O método **OnApplyChanges** copia esse valor na variável m \_ LVAL, substituindo o valor original:


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Em seguida: [etapa 9. Desconecte a página de propriedades](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



