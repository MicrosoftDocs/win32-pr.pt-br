---
title: Alça de tamanho (referência de elemento de interface do usuário do MSAA)
description: A alça de tamanho é um ponteiro especial do mouse no canto inferior direito de uma janela que permite que um usuário clique e arraste a alça de tamanho para redimensionar a janela.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7315425720ddee8beaf0f7c1f1b2ecbd8ba0fada51e64dc70453f3bb477e1f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795636"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Alça de tamanho (referência de elemento de interface do usuário do MSAA)

A alça de tamanho é um ponteiro especial do mouse no canto inferior direito de uma janela que permite que um usuário clique e arraste a alça de tamanho para redimensionar a janela.

## <a name="iaccessible-methods"></a>Métodos IAccessible

A alça de tamanho dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

A alça de tamanho dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                   | Comentários                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | A propriedade **Description** é "pode ser usada para redimensionar a largura e a altura de uma janela".                                                                                   |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | A propriedade **nome** é "tamanho da caixa".                                                                                                                                   |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | A janela que contém a alça de tamanho.                                                                                                                                |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | A propriedade **role** é [**\_ \_ alça do sistema de função**](object-roles.md).                                                                                  |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | O valor da propriedade de **estado** é zero, o que significa que o objeto está visível ou o [**estado do sistema é \_ \_ invisível**](object-state-constants.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




