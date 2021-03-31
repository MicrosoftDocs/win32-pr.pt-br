---
title: Alça de tamanho (referência de elemento de interface do usuário do MSAA)
description: A alça de tamanho é um ponteiro especial do mouse no canto inferior direito de uma janela que permite que um usuário clique e arraste a alça de tamanho para redimensionar a janela.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637113"
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

 

 




