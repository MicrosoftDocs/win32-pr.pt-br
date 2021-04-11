---
description: O código do produto é um GUID que é a principal identificação de um aplicativo ou produto.
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: Códigos de produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edca03d54dcd14068e89b2314b729e672b0c631c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170956"
---
# <a name="product-codes"></a>Códigos de produto

O código do produto é um GUID que é a principal identificação de um aplicativo ou produto. Para obter mais informações, consulte a propriedade [**ProductCode**](productcode.md) . Se forem feitas alterações significativas em um produto, o código do produto também deverá ser alterado para refletir isso. No entanto, não é um requisito de que o código do produto seja alterado se as alterações no produto forem relativamente secundárias.

As versões de 32 bits e 64 bits do pacote de um aplicativo devem ter códigos de produto diferentes. Se qualquer componente de 32 bits de um aplicativo for recompilado em um componente de 64 bits, um novo código de produto deverá ser atribuído.

Se um servidor exposto na [tabela PublishComponent](publishcomponent-table.md) for recompilado de 32 bits para 64 bits, o GUID nesta tabela também poderá precisar ser alterado para que os clientes de 32 bits e de 64 bits possam identificar a categoria de componente qualificada apropriada. Nesse caso, o código do produto também deve ser alterado.

Observe que as letras em GUIDs de código do produto devem estar em letras maiúsculas. Utilitários como o GUIDGEN geram GUIDs contendo letras minúsculas. As letras minúsculas nesses GUIDs devem ser alteradas para letras maiúsculas para serem usadas como código do produto ou código do pacote. Para obter mais informações, consulte [alterando o código do produto](changing-the-product-code.md).

O código do pacote é um GUID que identifica um determinado [*pacote*](p-gly.md)de Windows Installer. O código do pacote associa um arquivo. msi a um aplicativo ou produto e também pode ser usado para a verificação de fontes. Os códigos do produto e do pacote não são intercambiáveis. Dois arquivos. msi não idênticos já devem ter o mesmo código de pacote. Embora seja comum enviar um aplicativo que tenha o mesmo código de pacote e código do produto, os dois valores podem divergir à medida que o aplicativo é atualizado. Para obter mais informações, consulte [Package codes](package-codes.md).

 

 



