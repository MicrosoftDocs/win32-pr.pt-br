---
title: Propriedade Value
description: A propriedade Value fornece uma representação textual das informações visuais contidas em um objeto. Nem todos os objetos dão suporte à propriedade Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292245"
---
# <a name="value-property"></a>Propriedade Value

A propriedade **Value** fornece uma representação textual das informações visuais contidas em um objeto. Nem todos os objetos dão suporte à propriedade **Value** .

A propriedade **Value** é recuperada chamando [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

A propriedade **Value** informa ao cliente sobre as informações visuais contidas em um objeto. Por exemplo, um valor de controle de edição é o texto que ele contém, enquanto que um item de menu não tem nenhum valor.

## <a name="providing-hierarchical-information"></a>Fornecendo informações hierárquicas

A propriedade **Value** fornece informações hierárquicas em casos como um controle de exibição de árvore. Embora o objeto pai no controle de exibição de árvore não forneça informações na propriedade **Value** , cada item dentro do controle tem um valor de base zero que representa seu nível dentro da hierarquia. Itens de nível superior têm um valor de zero, itens de segundo nível têm um valor de um, e assim por diante.

 

 




