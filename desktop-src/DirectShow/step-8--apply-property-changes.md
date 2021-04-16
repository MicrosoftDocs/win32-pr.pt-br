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

 

 



