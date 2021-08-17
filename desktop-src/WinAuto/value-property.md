---
title: Propriedade Value
description: A propriedade Value fornece uma representação textual das informações visuais contidas em um objeto. Nem todos os objetos dão suporte à propriedade Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcebf689016add11008b5d8249ce4eaa8adf4a99a406afea8d1267f01f94201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133269"
---
# <a name="value-property"></a>Propriedade Value

A propriedade **Value** fornece uma representação textual das informações visuais contidas em um objeto. Nem todos os objetos dão suporte à propriedade **Value** .

A propriedade **Value** é recuperada chamando [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

A propriedade **Value** informa ao cliente sobre as informações visuais contidas em um objeto. Por exemplo, um valor de controle de edição é o texto que ele contém, enquanto que um item de menu não tem nenhum valor.

## <a name="providing-hierarchical-information"></a>Fornecendo informações hierárquicas

A propriedade **Value** fornece informações hierárquicas em casos como um controle de exibição de árvore. Embora o objeto pai no controle de exibição de árvore não forneça informações na propriedade **Value** , cada item dentro do controle tem um valor de base zero que representa seu nível dentro da hierarquia. Itens de nível superior têm um valor de zero, itens de segundo nível têm um valor de um, e assim por diante.

 

 




